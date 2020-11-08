---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077896"
---
# <span data-ttu-id="4d7ef-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="4d7ef-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="4d7ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7ef-103">Опубликуйте новую версию чертежа.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="4d7ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d7ef-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d7ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d7ef-105">DESCRIPTION</span></span>
<span data-ttu-id="4d7ef-106">Опубликуйте новую версию определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="4d7ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d7ef-107">EXAMPLES</span></span>

### <span data-ttu-id="4d7ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d7ef-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="4d7ef-109">Опубликуйте новую версию определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="4d7ef-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d7ef-110">PARAMETERS</span></span>

### <span data-ttu-id="4d7ef-111">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="4d7ef-111">-Blueprint</span></span>
<span data-ttu-id="4d7ef-112">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7ef-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="4d7ef-113">-ChangeNote</span></span>
<span data-ttu-id="4d7ef-114">Заметки, описывающие содержимое этой версии чертежа.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="4d7ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7ef-115">-DefaultProfile</span></span>
<span data-ttu-id="4d7ef-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d7ef-117">-Version</span><span class="sxs-lookup"><span data-stu-id="4d7ef-117">-Version</span></span>
<span data-ttu-id="4d7ef-118">Версия определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="4d7ef-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d7ef-119">-Confirm</span></span>
<span data-ttu-id="4d7ef-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d7ef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d7ef-121">-WhatIf</span></span>
<span data-ttu-id="4d7ef-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d7ef-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d7ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7ef-124">CommonParameters</span></span>
<span data-ttu-id="4d7ef-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7ef-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d7ef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7ef-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d7ef-127">INPUTS</span></span>

### <span data-ttu-id="4d7ef-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4d7ef-128">System.String</span></span>

### <span data-ttu-id="4d7ef-129">Microsoft. Azure. Commands. чертеж. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="4d7ef-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="4d7ef-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d7ef-130">OUTPUTS</span></span>

### <span data-ttu-id="4d7ef-131">Microsoft. Azure. Commands. чертеж. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="4d7ef-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="4d7ef-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d7ef-132">NOTES</span></span>

## <span data-ttu-id="4d7ef-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d7ef-133">RELATED LINKS</span></span>