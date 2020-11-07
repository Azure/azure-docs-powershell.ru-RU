---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913682"
---
# <span data-ttu-id="aeef2-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="aeef2-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="aeef2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aeef2-102">SYNOPSIS</span></span>
<span data-ttu-id="aeef2-103">Получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="aeef2-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeef2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aeef2-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeef2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeef2-105">DESCRIPTION</span></span>
<span data-ttu-id="aeef2-106">Командлет **Get-AzureRmSnapshot** получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="aeef2-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="aeef2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aeef2-107">EXAMPLES</span></span>

### <span data-ttu-id="aeef2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aeef2-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="aeef2-109">Эта команда получает свойства всех снимков подписки.</span><span class="sxs-lookup"><span data-stu-id="aeef2-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="aeef2-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aeef2-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="aeef2-111">Эта команда получает свойства всех моментальных снимков в группе ресурсов с именем "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="aeef2-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="aeef2-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="aeef2-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="aeef2-113">Эта команда получает свойства моментального снимка "SnapshotName1" в группе ресурсов с именем "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="aeef2-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="aeef2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aeef2-114">PARAMETERS</span></span>

### <span data-ttu-id="aeef2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeef2-115">-DefaultProfile</span></span>
<span data-ttu-id="aeef2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aeef2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeef2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeef2-117">-ResourceGroupName</span></span>
<span data-ttu-id="aeef2-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aeef2-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aeef2-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="aeef2-119">-SnapshotName</span></span>
<span data-ttu-id="aeef2-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="aeef2-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="aeef2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeef2-121">CommonParameters</span></span>
<span data-ttu-id="aeef2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aeef2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeef2-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeef2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeef2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aeef2-124">INPUTS</span></span>

### <span data-ttu-id="aeef2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="aeef2-125">System.String</span></span>

## <span data-ttu-id="aeef2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeef2-126">OUTPUTS</span></span>

### <span data-ttu-id="aeef2-127">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="aeef2-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="aeef2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="aeef2-128">NOTES</span></span>

## <span data-ttu-id="aeef2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aeef2-129">RELATED LINKS</span></span>

