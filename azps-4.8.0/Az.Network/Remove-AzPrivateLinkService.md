---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236014"
---
# <span data-ttu-id="82b71-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82b71-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="82b71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82b71-102">SYNOPSIS</span></span>
<span data-ttu-id="82b71-103">Удаление службы частной ссылки</span><span class="sxs-lookup"><span data-stu-id="82b71-103">Removes a private link service</span></span>

## <span data-ttu-id="82b71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82b71-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82b71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b71-105">DESCRIPTION</span></span>
<span data-ttu-id="82b71-106">Командлет **Remove-AzPrivateLinkService** Удаляет службу частной ссылки</span><span class="sxs-lookup"><span data-stu-id="82b71-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="82b71-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82b71-107">EXAMPLES</span></span>

### <span data-ttu-id="82b71-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82b71-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="82b71-109">В этом примере удаляется служба частной ссылки с именем TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="82b71-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="82b71-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82b71-110">PARAMETERS</span></span>

### <span data-ttu-id="82b71-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82b71-111">-AsJob</span></span>
<span data-ttu-id="82b71-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="82b71-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82b71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b71-113">-DefaultProfile</span></span>
<span data-ttu-id="82b71-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82b71-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b71-115">-Force</span><span class="sxs-lookup"><span data-stu-id="82b71-115">-Force</span></span>
<span data-ttu-id="82b71-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="82b71-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="82b71-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82b71-117">-Name</span></span>
<span data-ttu-id="82b71-118">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="82b71-118">The name of the service.</span></span>

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

### <span data-ttu-id="82b71-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82b71-119">-PassThru</span></span>
<span data-ttu-id="82b71-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="82b71-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82b71-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="82b71-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82b71-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b71-122">-ResourceGroupName</span></span>
<span data-ttu-id="82b71-123">Имя группы ресурсов для службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="82b71-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="82b71-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82b71-124">-Confirm</span></span>
<span data-ttu-id="82b71-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82b71-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b71-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82b71-126">-WhatIf</span></span>
<span data-ttu-id="82b71-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82b71-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b71-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82b71-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b71-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b71-129">CommonParameters</span></span>
<span data-ttu-id="82b71-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82b71-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b71-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82b71-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b71-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82b71-132">INPUTS</span></span>

### <span data-ttu-id="82b71-133">System. String</span><span class="sxs-lookup"><span data-stu-id="82b71-133">System.String</span></span>

## <span data-ttu-id="82b71-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b71-134">OUTPUTS</span></span>

### <span data-ttu-id="82b71-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82b71-135">System.Boolean</span></span>

## <span data-ttu-id="82b71-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="82b71-136">NOTES</span></span>

## <span data-ttu-id="82b71-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82b71-137">RELATED LINKS</span></span>

[<span data-ttu-id="82b71-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82b71-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="82b71-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="82b71-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)