---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 9de25adae04afd0f09a2a09118c55d4e679a44db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903418"
---
# <span data-ttu-id="c468a-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c468a-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="c468a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c468a-102">SYNOPSIS</span></span>
<span data-ttu-id="c468a-103">Удаляет подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c468a-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="c468a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c468a-104">SYNTAX</span></span>

### <span data-ttu-id="c468a-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c468a-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c468a-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="c468a-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection [-Force] [-AsJob] [-PassThru] -Name <String> -ServiceName <String>
 -ResourceGroupName <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c468a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c468a-107">DESCRIPTION</span></span>
<span data-ttu-id="c468a-108">Командлет **Remove-AzPrivateEndpointConnection** удаляет подключение к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c468a-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span> 

## <span data-ttu-id="c468a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c468a-109">EXAMPLES</span></span>

### <span data-ttu-id="c468a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c468a-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="c468a-111">В этом примере удаляется подключение к частной конечной точке с именем MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="c468a-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="c468a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c468a-112">PARAMETERS</span></span>

### <span data-ttu-id="c468a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c468a-113">-AsJob</span></span>
<span data-ttu-id="c468a-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c468a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c468a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c468a-115">-DefaultProfile</span></span>
<span data-ttu-id="c468a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c468a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c468a-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="c468a-117">-Description</span></span>
<span data-ttu-id="c468a-118">Причина действия.</span><span class="sxs-lookup"><span data-stu-id="c468a-118">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c468a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c468a-119">-Force</span></span>
<span data-ttu-id="c468a-120">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="c468a-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="c468a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c468a-121">-Name</span></span>
<span data-ttu-id="c468a-122">Имя подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c468a-122">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c468a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c468a-123">-PassThru</span></span>
<span data-ttu-id="c468a-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="c468a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c468a-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c468a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c468a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c468a-126">-ResourceGroupName</span></span>
<span data-ttu-id="c468a-127">Имя группы ресурсов для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c468a-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c468a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c468a-128">-ResourceId</span></span>
<span data-ttu-id="c468a-129">Идентификатор диспетчера ресурсов Azure для подключения к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c468a-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="c468a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c468a-130">-ServiceName</span></span>
<span data-ttu-id="c468a-131">Имя службы частной ссылки с подключением к частной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c468a-131">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="c468a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c468a-132">-Confirm</span></span>
<span data-ttu-id="c468a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c468a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c468a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c468a-134">-WhatIf</span></span>
<span data-ttu-id="c468a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c468a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c468a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c468a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c468a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c468a-137">CommonParameters</span></span>
<span data-ttu-id="c468a-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c468a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c468a-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c468a-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c468a-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c468a-140">INPUTS</span></span>

### <span data-ttu-id="c468a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c468a-141">System.String</span></span>

## <span data-ttu-id="c468a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c468a-142">OUTPUTS</span></span>

### <span data-ttu-id="c468a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c468a-143">System.Boolean</span></span>

## <span data-ttu-id="c468a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c468a-144">NOTES</span></span>

## <span data-ttu-id="c468a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c468a-145">RELATED LINKS</span></span>

[<span data-ttu-id="c468a-146">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c468a-146">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
