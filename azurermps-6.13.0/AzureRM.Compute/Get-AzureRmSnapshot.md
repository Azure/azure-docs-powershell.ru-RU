---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 14b1c1179e9fee15f398c4518e446cf47396e660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561060"
---
# <span data-ttu-id="d2adb-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d2adb-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="d2adb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2adb-102">SYNOPSIS</span></span>
<span data-ttu-id="d2adb-103">Получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="d2adb-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2adb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2adb-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2adb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2adb-105">DESCRIPTION</span></span>
<span data-ttu-id="d2adb-106">Командлет **Get-AzureRmSnapshot** получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="d2adb-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="d2adb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2adb-107">EXAMPLES</span></span>

### <span data-ttu-id="d2adb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2adb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="d2adb-109">Эта команда получает свойства всех снимков подписки.</span><span class="sxs-lookup"><span data-stu-id="d2adb-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="d2adb-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d2adb-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="d2adb-111">Эта команда получает свойства всех моментальных снимков в группе ресурсов с именем "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="d2adb-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="d2adb-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d2adb-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="d2adb-113">Эта команда получает свойства моментального снимка "SnapshotName1" в группе ресурсов с именем "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="d2adb-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="d2adb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2adb-114">PARAMETERS</span></span>

### <span data-ttu-id="d2adb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2adb-115">-DefaultProfile</span></span>
<span data-ttu-id="d2adb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2adb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2adb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2adb-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2adb-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2adb-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2adb-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d2adb-119">-SnapshotName</span></span>
<span data-ttu-id="d2adb-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="d2adb-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="d2adb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2adb-121">CommonParameters</span></span>
<span data-ttu-id="d2adb-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2adb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2adb-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2adb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2adb-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2adb-124">INPUTS</span></span>

### <span data-ttu-id="d2adb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d2adb-125">System.String</span></span>

## <span data-ttu-id="d2adb-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2adb-126">OUTPUTS</span></span>

### <span data-ttu-id="d2adb-127">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d2adb-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d2adb-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2adb-128">NOTES</span></span>

## <span data-ttu-id="d2adb-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2adb-129">RELATED LINKS</span></span>
