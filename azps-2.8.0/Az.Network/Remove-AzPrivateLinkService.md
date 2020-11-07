---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 3b0ba9527ca7d0354429a90439bbe33d973bf550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901925"
---
# <span data-ttu-id="0b97b-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b97b-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="0b97b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b97b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b97b-103">Удаление службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="0b97b-103">Removes a private link service</span></span>

## <span data-ttu-id="0b97b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b97b-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b97b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b97b-105">DESCRIPTION</span></span>
<span data-ttu-id="0b97b-106">Командлет **Remove-AzPrivateLinkService** Удаляет службу частной ссылки</span><span class="sxs-lookup"><span data-stu-id="0b97b-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="0b97b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b97b-107">EXAMPLES</span></span>

### <span data-ttu-id="0b97b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b97b-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="0b97b-109">В этом примере удаляется служба частной ссылки с именем TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="0b97b-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="0b97b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b97b-110">PARAMETERS</span></span>

### <span data-ttu-id="0b97b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b97b-111">-AsJob</span></span>
<span data-ttu-id="0b97b-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0b97b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b97b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b97b-113">-DefaultProfile</span></span>
<span data-ttu-id="0b97b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b97b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b97b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0b97b-115">-Force</span></span>
<span data-ttu-id="0b97b-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="0b97b-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="0b97b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b97b-117">-Name</span></span>
<span data-ttu-id="0b97b-118">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="0b97b-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b97b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b97b-119">-PassThru</span></span>
<span data-ttu-id="0b97b-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0b97b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0b97b-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0b97b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0b97b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b97b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0b97b-123">Имя группы ресурсов для службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="0b97b-123">The resource group name of the private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b97b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b97b-124">-Confirm</span></span>
<span data-ttu-id="0b97b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b97b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b97b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b97b-126">-WhatIf</span></span>
<span data-ttu-id="0b97b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b97b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b97b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b97b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b97b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b97b-129">CommonParameters</span></span>
<span data-ttu-id="0b97b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b97b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b97b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b97b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b97b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b97b-132">INPUTS</span></span>

### <span data-ttu-id="0b97b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0b97b-133">System.String</span></span>

## <span data-ttu-id="0b97b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b97b-134">OUTPUTS</span></span>

### <span data-ttu-id="0b97b-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b97b-135">System.Boolean</span></span>

## <span data-ttu-id="0b97b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b97b-136">NOTES</span></span>

## <span data-ttu-id="0b97b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b97b-137">RELATED LINKS</span></span>

[<span data-ttu-id="0b97b-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b97b-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="0b97b-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0b97b-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)