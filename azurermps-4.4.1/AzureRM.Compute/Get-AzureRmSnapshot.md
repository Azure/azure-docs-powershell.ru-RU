---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 98297d46416b23cd127e5ab5b65ce2fcfac38aa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560487"
---
# <span data-ttu-id="6965a-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="6965a-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="6965a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6965a-102">SYNOPSIS</span></span>
<span data-ttu-id="6965a-103">Получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="6965a-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6965a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6965a-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6965a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6965a-105">DESCRIPTION</span></span>
<span data-ttu-id="6965a-106">Командлет **Get-AzureRmSnapshot** получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="6965a-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="6965a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6965a-107">EXAMPLES</span></span>

### <span data-ttu-id="6965a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6965a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="6965a-109">Эта команда получает свойства всех снимков подписки.</span><span class="sxs-lookup"><span data-stu-id="6965a-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="6965a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6965a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="6965a-111">Эта команда получает свойства всех моментальных снимков в группе ресурсов с именем "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="6965a-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="6965a-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6965a-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="6965a-113">Эта команда получает свойства моментального снимка "SnapshotName1" в группе ресурсов с именем "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="6965a-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="6965a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6965a-114">PARAMETERS</span></span>

### <span data-ttu-id="6965a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6965a-115">-DefaultProfile</span></span>
<span data-ttu-id="6965a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6965a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6965a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6965a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6965a-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6965a-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965a-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="6965a-119">-SnapshotName</span></span>
<span data-ttu-id="6965a-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="6965a-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6965a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6965a-121">CommonParameters</span></span>
<span data-ttu-id="6965a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6965a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6965a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6965a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6965a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6965a-124">INPUTS</span></span>

### <span data-ttu-id="6965a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6965a-125">System.String</span></span>

## <span data-ttu-id="6965a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6965a-126">OUTPUTS</span></span>

### <span data-ttu-id="6965a-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="6965a-127">System.Object</span></span>

## <span data-ttu-id="6965a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6965a-128">NOTES</span></span>

## <span data-ttu-id="6965a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6965a-129">RELATED LINKS</span></span>

