vi ../../templates/route.yaml
apiVersion: route.openshift.io/v1
kind: Route
metadata:
  name: {{ .Release.Name }}
spec:
  to:
    kind: Service
    name: {{ .Release.Name }}
  {{- if .Values.secureRoute }}
  tls:
    termination: edge
  {{- end }}
