---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065461"
---
# <span data-ttu-id="e2f99-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="e2f99-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="e2f99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2f99-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f99-103">Опубликуйте новую версию чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2f99-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="e2f99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2f99-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2f99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f99-105">DESCRIPTION</span></span>
<span data-ttu-id="e2f99-106">Опубликуйте новую версию определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2f99-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e2f99-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f99-107">EXAMPLES</span></span>

### <span data-ttu-id="e2f99-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2f99-108">Example 1</span></span>
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
<span data-ttu-id="e2f99-109">Опубликуйте новую версию определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2f99-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="e2f99-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f99-110">PARAMETERS</span></span>

### <span data-ttu-id="e2f99-111">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="e2f99-111">-Blueprint</span></span>
<span data-ttu-id="e2f99-112">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2f99-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f99-113">-DefaultProfile</span></span>
<span data-ttu-id="e2f99-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f99-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f99-115">-Version</span><span class="sxs-lookup"><span data-stu-id="e2f99-115">-Version</span></span>
<span data-ttu-id="e2f99-116">Версия определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2f99-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="e2f99-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="e2f99-117">-ChangeNote</span></span>
<span data-ttu-id="e2f99-118">Заметки, описывающие содержимое этой версии чертежа.</span><span class="sxs-lookup"><span data-stu-id="e2f99-118">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f99-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f99-119">CommonParameters</span></span>
<span data-ttu-id="e2f99-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2f99-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e2f99-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f99-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f99-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2f99-122">INPUTS</span></span>

### <span data-ttu-id="e2f99-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e2f99-123">System.String</span></span>

### <span data-ttu-id="e2f99-124">Microsoft. Azure. Commands. чертеж. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="e2f99-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="e2f99-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f99-125">OUTPUTS</span></span>

### <span data-ttu-id="e2f99-126">Microsoft. Azure. Commands. чертеж. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="e2f99-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="e2f99-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2f99-127">NOTES</span></span>

## <span data-ttu-id="e2f99-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f99-128">RELATED LINKS</span></span>
