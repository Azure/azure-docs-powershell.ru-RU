---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404588"
---
# <span data-ttu-id="583e2-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="583e2-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="583e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="583e2-102">SYNOPSIS</span></span>
<span data-ttu-id="583e2-103">Удаляет личную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="583e2-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="583e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="583e2-104">SYNTAX</span></span>

### <span data-ttu-id="583e2-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="583e2-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="583e2-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="583e2-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="583e2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="583e2-107">DESCRIPTION</span></span>
<span data-ttu-id="583e2-108">Для удаления подключения к закрытой конечной точке удаляется **cmdlet Remove-AzPrivateEndpointConnection.**</span><span class="sxs-lookup"><span data-stu-id="583e2-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="583e2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="583e2-109">EXAMPLES</span></span>

### <span data-ttu-id="583e2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="583e2-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="583e2-111">В этом примере удаляется частное подключение конечной точки MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="583e2-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="583e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="583e2-112">PARAMETERS</span></span>

### <span data-ttu-id="583e2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="583e2-113">-AsJob</span></span>
<span data-ttu-id="583e2-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="583e2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="583e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583e2-115">-DefaultProfile</span></span>
<span data-ttu-id="583e2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="583e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="583e2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="583e2-117">-Force</span></span>
<span data-ttu-id="583e2-118">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="583e2-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="583e2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="583e2-119">-Name</span></span>
<span data-ttu-id="583e2-120">Имя подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="583e2-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="583e2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="583e2-121">-PassThru</span></span>
<span data-ttu-id="583e2-122">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="583e2-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="583e2-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="583e2-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="583e2-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="583e2-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="583e2-125">Тип ресурса private link.</span><span class="sxs-lookup"><span data-stu-id="583e2-125">The private link resource type.</span></span>

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

### <span data-ttu-id="583e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="583e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="583e2-127">Имя группы ресурсов подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="583e2-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="583e2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="583e2-128">-ResourceId</span></span>
<span data-ttu-id="583e2-129">ИД диспетчера ресурсов Azure для подключения к закрытой конечной точке.</span><span class="sxs-lookup"><span data-stu-id="583e2-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="583e2-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="583e2-130">-ServiceName</span></span>
<span data-ttu-id="583e2-131">Имя службы, к которую относится частное подключение конечной точки.</span><span class="sxs-lookup"><span data-stu-id="583e2-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="583e2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="583e2-132">-Confirm</span></span>
<span data-ttu-id="583e2-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="583e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="583e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="583e2-134">-WhatIf</span></span>
<span data-ttu-id="583e2-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="583e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="583e2-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="583e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="583e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583e2-137">CommonParameters</span></span>
<span data-ttu-id="583e2-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="583e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583e2-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="583e2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583e2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="583e2-140">INPUTS</span></span>

### <span data-ttu-id="583e2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="583e2-141">System.String</span></span>

## <span data-ttu-id="583e2-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="583e2-142">OUTPUTS</span></span>

### <span data-ttu-id="583e2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="583e2-143">System.Boolean</span></span>

## <span data-ttu-id="583e2-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="583e2-144">NOTES</span></span>

## <span data-ttu-id="583e2-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="583e2-145">RELATED LINKS</span></span>

[<span data-ttu-id="583e2-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="583e2-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="583e2-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="583e2-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="583e2-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="583e2-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="583e2-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="583e2-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
