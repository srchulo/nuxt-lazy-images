<script>
export default {
  functional: true,
  props: {
    tag: {
      type: String,
      required: true
    },
    src: {
      type: Object,
      required: true
    }
  },
  render(createElement, context) {
    return createElement(
      context.props.tag,
      {
        ...context.data,
        style: {
          ...context.data.style,
          'background-image': "url('" + context.props.src.placeholder + "')"
        },
        attrs: {
          ...context.data.attrs,
          'lazy-background': context.props.src.src
        },
        directives: [
          {
            name: 'lazy-background',
            value: context.props.src.src
          }
        ]
      },
      context.children
    )
  }
}
</script>
