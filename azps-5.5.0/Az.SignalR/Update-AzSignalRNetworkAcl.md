---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242061"
---
# <span data-ttu-id="c7c2f-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="c7c2f-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="c7c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c2f-103">Обновив network ACL службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="c7c2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7c2f-104">SYNTAX</span></span>

### <span data-ttu-id="c7c2f-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7c2f-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c2f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c2f-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c2f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7c2f-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c2f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7c2f-108">DESCRIPTION</span></span>
<span data-ttu-id="c7c2f-109">Обновление сетевого ACL службы SignalR, включая действие по умолчанию и сетевые acls для подключения к общедоступным и частным сетям.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="c7c2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7c2f-110">EXAMPLES</span></span>

### <span data-ttu-id="c7c2f-111">Разрешить RESTAPI,ClientConnection для общедоступных сетей и установить для действия по умолчанию запрет</span><span class="sxs-lookup"><span data-stu-id="c7c2f-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="c7c2f-112">Разрешение клиентского подключения и подключения к серверу для подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="c7c2f-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="c7c2f-113">Запретить клиентскую подключение как для общедоступных сетей, так и для частных конечных точек.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="c7c2f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7c2f-114">PARAMETERS</span></span>

### <span data-ttu-id="c7c2f-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="c7c2f-115">-Allow</span></span>
<span data-ttu-id="c7c2f-116">Разрешенные сетевые ALS</span><span class="sxs-lookup"><span data-stu-id="c7c2f-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7c2f-117">-AsJob</span></span>
<span data-ttu-id="c7c2f-118">Запустите проектлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-118">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="c7c2f-119">-DefaultAction</span></span>
<span data-ttu-id="c7c2f-120">Действие по умолчанию сетевых ALS SignalR, разрешать или от запретить.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="c7c2f-121">Он решает, следует ли запретить ALS сети или разрешить ее действие.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="c7c2f-122">Например, если по умолчанию разрешается действие, имеет значение только запрет на ALS.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c2f-123">-DefaultProfile</span></span>
<span data-ttu-id="c7c2f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="c7c2f-125">-Deny</span></span>
<span data-ttu-id="c7c2f-126">Отклонение ALS сети</span><span class="sxs-lookup"><span data-stu-id="c7c2f-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7c2f-127">-InputObject</span></span>
<span data-ttu-id="c7c2f-128">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c7c2f-129">-Name</span></span>
<span data-ttu-id="c7c2f-130">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="c7c2f-131">-PrivateEndpointName</span></span>
<span data-ttu-id="c7c2f-132">Имена частных конечных точек, которые требуется обновить</span><span class="sxs-lookup"><span data-stu-id="c7c2f-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="c7c2f-133">-PublicNetwork</span></span>
<span data-ttu-id="c7c2f-134">Обновление ALS общедоступных сетей</span><span class="sxs-lookup"><span data-stu-id="c7c2f-134">Update public network ACLs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c2f-135">-ResourceGroupName</span></span>
<span data-ttu-id="c7c2f-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-136">The resource group name.</span></span>
<span data-ttu-id="c7c2f-137">Значение по умолчанию будет использоваться, если не указано.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7c2f-138">-ResourceId</span></span>
<span data-ttu-id="c7c2f-139">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7c2f-140">-Confirm</span></span>
<span data-ttu-id="c7c2f-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c2f-142">-WhatIf</span></span>
<span data-ttu-id="c7c2f-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c2f-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c2f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c2f-145">CommonParameters</span></span>
<span data-ttu-id="c7c2f-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c2f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c2f-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7c2f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c2f-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7c2f-148">INPUTS</span></span>

### <span data-ttu-id="c7c2f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c7c2f-149">System.String</span></span>

## <span data-ttu-id="c7c2f-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7c2f-150">OUTPUTS</span></span>

### <span data-ttu-id="c7c2f-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="c7c2f-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="c7c2f-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7c2f-152">NOTES</span></span>

## <span data-ttu-id="c7c2f-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7c2f-153">RELATED LINKS</span></span>
