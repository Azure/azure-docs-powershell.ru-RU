---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: be060c320c05b44a4b0d8f79b519f63e4dd47bcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996148"
---
# <span data-ttu-id="3fe4d-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3fe4d-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="3fe4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fe4d-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe4d-103">Удаляет личную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="3fe4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3fe4d-104">SYNTAX</span></span>

### <span data-ttu-id="3fe4d-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3fe4d-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fe4d-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="3fe4d-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fe4d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3fe4d-107">DESCRIPTION</span></span>
<span data-ttu-id="3fe4d-108">Для удаления подключения к закрытой конечной точке удаляется **cmdlet Remove-AzPrivateEndpointConnection.**</span><span class="sxs-lookup"><span data-stu-id="3fe4d-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="3fe4d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3fe4d-109">EXAMPLES</span></span>

### <span data-ttu-id="3fe4d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3fe4d-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="3fe4d-111">В этом примере удаляется частное подключение конечной точки MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="3fe4d-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="3fe4d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fe4d-112">PARAMETERS</span></span>

### <span data-ttu-id="3fe4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fe4d-113">-AsJob</span></span>
<span data-ttu-id="3fe4d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3fe4d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fe4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe4d-115">-DefaultProfile</span></span>
<span data-ttu-id="3fe4d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe4d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3fe4d-117">-Force</span></span>
<span data-ttu-id="3fe4d-118">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="3fe4d-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3fe4d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3fe4d-119">-Name</span></span>
<span data-ttu-id="3fe4d-120">Имя подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe4d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fe4d-121">-PassThru</span></span>
<span data-ttu-id="3fe4d-122">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3fe4d-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fe4d-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="3fe4d-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="3fe4d-125">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fe4d-127">Имя группы ресурсов подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe4d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fe4d-128">-ResourceId</span></span>
<span data-ttu-id="3fe4d-129">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe4d-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3fe4d-130">-ServiceName</span></span>
<span data-ttu-id="3fe4d-131">Имя службы, к которую относится частное подключение конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fe4d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fe4d-132">-Confirm</span></span>
<span data-ttu-id="3fe4d-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe4d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe4d-134">-WhatIf</span></span>
<span data-ttu-id="3fe4d-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fe4d-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe4d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe4d-137">CommonParameters</span></span>
<span data-ttu-id="3fe4d-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe4d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe4d-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fe4d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe4d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fe4d-140">INPUTS</span></span>

### <span data-ttu-id="3fe4d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3fe4d-141">System.String</span></span>

## <span data-ttu-id="3fe4d-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3fe4d-142">OUTPUTS</span></span>

### <span data-ttu-id="3fe4d-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fe4d-143">System.Boolean</span></span>

## <span data-ttu-id="3fe4d-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3fe4d-144">NOTES</span></span>

## <span data-ttu-id="3fe4d-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3fe4d-145">RELATED LINKS</span></span>

[<span data-ttu-id="3fe4d-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3fe4d-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3fe4d-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3fe4d-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3fe4d-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3fe4d-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="3fe4d-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3fe4d-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
