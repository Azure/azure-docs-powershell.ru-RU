---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248106"
---
# <span data-ttu-id="6f855-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f855-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="6f855-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f855-102">SYNOPSIS</span></span>
<span data-ttu-id="6f855-103">Удаляет подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6f855-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="6f855-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f855-104">SYNTAX</span></span>

### <span data-ttu-id="6f855-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f855-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f855-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="6f855-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f855-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f855-107">DESCRIPTION</span></span>
<span data-ttu-id="6f855-108">Командлет **Remove-AzPrivateEndpointConnection** удаляет подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6f855-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="6f855-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f855-109">EXAMPLES</span></span>

### <span data-ttu-id="6f855-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f855-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="6f855-111">В этом примере удаляется подключение к частной конечной точке с именем MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="6f855-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="6f855-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f855-112">PARAMETERS</span></span>

### <span data-ttu-id="6f855-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f855-113">-AsJob</span></span>
<span data-ttu-id="6f855-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6f855-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f855-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f855-115">-DefaultProfile</span></span>
<span data-ttu-id="6f855-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f855-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f855-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6f855-117">-Force</span></span>
<span data-ttu-id="6f855-118">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="6f855-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="6f855-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f855-119">-Name</span></span>
<span data-ttu-id="6f855-120">Имя подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6f855-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="6f855-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f855-121">-PassThru</span></span>
<span data-ttu-id="6f855-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6f855-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f855-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6f855-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f855-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="6f855-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="6f855-125">Тип ресурса «частная ссылка».</span><span class="sxs-lookup"><span data-stu-id="6f855-125">The private link resource type.</span></span>

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

### <span data-ttu-id="6f855-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f855-126">-ResourceGroupName</span></span>
<span data-ttu-id="6f855-127">Имя группы ресурсов для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6f855-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="6f855-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f855-128">-ResourceId</span></span>
<span data-ttu-id="6f855-129">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6f855-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="6f855-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6f855-130">-ServiceName</span></span>
<span data-ttu-id="6f855-131">Имя службы, к которой принадлежит подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="6f855-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="6f855-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f855-132">-Confirm</span></span>
<span data-ttu-id="6f855-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f855-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f855-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f855-134">-WhatIf</span></span>
<span data-ttu-id="6f855-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f855-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f855-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f855-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f855-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f855-137">CommonParameters</span></span>
<span data-ttu-id="6f855-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f855-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f855-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f855-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f855-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f855-140">INPUTS</span></span>

### <span data-ttu-id="6f855-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6f855-141">System.String</span></span>

## <span data-ttu-id="6f855-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f855-142">OUTPUTS</span></span>

### <span data-ttu-id="6f855-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f855-143">System.Boolean</span></span>

## <span data-ttu-id="6f855-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f855-144">NOTES</span></span>

## <span data-ttu-id="6f855-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f855-145">RELATED LINKS</span></span>

[<span data-ttu-id="6f855-146">Утвердить — AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f855-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6f855-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f855-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6f855-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f855-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="6f855-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6f855-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)