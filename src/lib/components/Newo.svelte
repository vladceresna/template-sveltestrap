<script lang="js">
    import {
    Button,
    Card,
    CardBody,
    CardFooter,
    CardHeader,
    CardSubtitle,
    CardText,
    CardTitle,
    CardLink
  } from '@sveltestrap/sveltestrap';
  export let title;
  export let slogan;
  export let link;
</script>
<style>

</style>

<Card style="">
    <CardHeader style="color:white;background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(0,11,91,1) 23%, rgba(0,212,255,1) 100%);">
      <CardTitle>{title}</CardTitle>
    </CardHeader>
    <CardBody>
      <CardSubtitle>{slogan}</CardSubtitle>
      <CardText>
        <slot/>
        <br>Text <CardLink>{link}</CardLink>
      </CardText>
    </CardBody>
</Card>