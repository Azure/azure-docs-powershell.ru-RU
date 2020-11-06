---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565568"
---
# <span data-ttu-id="e5925-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="e5925-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="e5925-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5925-102">SYNOPSIS</span></span>
<span data-ttu-id="e5925-103">Получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="e5925-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5925-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5925-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5925-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5925-105">DESCRIPTION</span></span>
<span data-ttu-id="e5925-106">Командлет **Get-AzureRmSnapshot** получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="e5925-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="e5925-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5925-107">EXAMPLES</span></span>

### <span data-ttu-id="e5925-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5925-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="e5925-109">Эта команда получает свойства всех снимков подписки.</span><span class="sxs-lookup"><span data-stu-id="e5925-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="e5925-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5925-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="e5925-111">Эта команда получает свойства всех моментальных снимков в группе ресурсов с именем "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="e5925-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="e5925-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e5925-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="e5925-113">Эта команда получает свойства моментального снимка "SnapshotName1" в группе ресурсов с именем "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="e5925-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="e5925-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5925-114">PARAMETERS</span></span>

### <span data-ttu-id="e5925-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5925-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5925-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5925-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5925-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e5925-117">-SnapshotName</span></span>
<span data-ttu-id="e5925-118">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="e5925-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5925-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5925-119">CommonParameters</span></span>
<span data-ttu-id="e5925-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5925-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5925-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5925-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5925-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5925-122">INPUTS</span></span>

### <span data-ttu-id="e5925-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e5925-123">System.String</span></span>

## <span data-ttu-id="e5925-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5925-124">OUTPUTS</span></span>

### <span data-ttu-id="e5925-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="e5925-125">System.Object</span></span>

## <span data-ttu-id="e5925-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5925-126">NOTES</span></span>

## <span data-ttu-id="e5925-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5925-127">RELATED LINKS</span></span>

