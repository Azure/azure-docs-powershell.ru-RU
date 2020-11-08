---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080264"
---
# <span data-ttu-id="04dd2-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="04dd2-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="04dd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="04dd2-103">Обновите список ACL сети службы сигнальных служб.</span><span class="sxs-lookup"><span data-stu-id="04dd2-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="04dd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04dd2-104">SYNTAX</span></span>

### <span data-ttu-id="04dd2-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04dd2-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04dd2-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04dd2-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04dd2-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04dd2-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04dd2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04dd2-108">DESCRIPTION</span></span>
<span data-ttu-id="04dd2-109">Обновите список ACL сети службы сигнальных служб, включая действие по умолчанию и сетевые ACL для общедоступного и частного подключения.</span><span class="sxs-lookup"><span data-stu-id="04dd2-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="04dd2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04dd2-110">EXAMPLES</span></span>

### <span data-ttu-id="04dd2-111">Разрешить RESTAPI, ClientConnection для общедоступной сети и установить действие по умолчанию "запретить"</span><span class="sxs-lookup"><span data-stu-id="04dd2-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="04dd2-112">Разрешение подключения клиента и подключения сервера к частной конечной точке</span><span class="sxs-lookup"><span data-stu-id="04dd2-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="04dd2-113">Запрет подключения клиента как к общедоступной сети, так и к частной конечной точке</span><span class="sxs-lookup"><span data-stu-id="04dd2-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="04dd2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04dd2-114">PARAMETERS</span></span>

### <span data-ttu-id="04dd2-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="04dd2-115">-Allow</span></span>
<span data-ttu-id="04dd2-116">Разрешенные сетевые ACL</span><span class="sxs-lookup"><span data-stu-id="04dd2-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="04dd2-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04dd2-117">-AsJob</span></span>
<span data-ttu-id="04dd2-118">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="04dd2-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="04dd2-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="04dd2-119">-DefaultAction</span></span>
<span data-ttu-id="04dd2-120">Действие по умолчанию списков ACL сети SignalR, разрешено или запрещено.</span><span class="sxs-lookup"><span data-stu-id="04dd2-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="04dd2-121">Вы решите, нужно ли отклонять сетевые ACL или разрешить использование ACL сети.</span><span class="sxs-lookup"><span data-stu-id="04dd2-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="04dd2-122">Например, если разрешено действие по умолчанию, то это не относится к отклонениям ACL.</span><span class="sxs-lookup"><span data-stu-id="04dd2-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="04dd2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dd2-123">-DefaultProfile</span></span>
<span data-ttu-id="04dd2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04dd2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04dd2-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="04dd2-125">-Deny</span></span>
<span data-ttu-id="04dd2-126">Отказано в доступе к сетевым ACL</span><span class="sxs-lookup"><span data-stu-id="04dd2-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="04dd2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04dd2-127">-InputObject</span></span>
<span data-ttu-id="04dd2-128">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="04dd2-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="04dd2-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04dd2-129">-Name</span></span>
<span data-ttu-id="04dd2-130">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="04dd2-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="04dd2-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="04dd2-131">-PrivateEndpointName</span></span>
<span data-ttu-id="04dd2-132">Имена (-ов) закрытых конечных точек, которые нужно обновить</span><span class="sxs-lookup"><span data-stu-id="04dd2-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="04dd2-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="04dd2-133">-PublicNetwork</span></span>
<span data-ttu-id="04dd2-134">Обновление списков ACL общедоступной сети</span><span class="sxs-lookup"><span data-stu-id="04dd2-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="04dd2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04dd2-135">-ResourceGroupName</span></span>
<span data-ttu-id="04dd2-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04dd2-136">The resource group name.</span></span>
<span data-ttu-id="04dd2-137">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="04dd2-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="04dd2-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04dd2-138">-ResourceId</span></span>
<span data-ttu-id="04dd2-139">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="04dd2-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="04dd2-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04dd2-140">-Confirm</span></span>
<span data-ttu-id="04dd2-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04dd2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04dd2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04dd2-142">-WhatIf</span></span>
<span data-ttu-id="04dd2-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04dd2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04dd2-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04dd2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04dd2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dd2-145">CommonParameters</span></span>
<span data-ttu-id="04dd2-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04dd2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dd2-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04dd2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dd2-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04dd2-148">INPUTS</span></span>

### <span data-ttu-id="04dd2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="04dd2-149">System.String</span></span>

## <span data-ttu-id="04dd2-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04dd2-150">OUTPUTS</span></span>

### <span data-ttu-id="04dd2-151">Microsoft. Azure. Commands. SignalR. Models. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="04dd2-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="04dd2-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="04dd2-152">NOTES</span></span>

## <span data-ttu-id="04dd2-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04dd2-153">RELATED LINKS</span></span>