---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911556"
---
# <span data-ttu-id="caeeb-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="caeeb-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="caeeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="caeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="caeeb-103">Получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="caeeb-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="caeeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="caeeb-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caeeb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caeeb-105">DESCRIPTION</span></span>
<span data-ttu-id="caeeb-106">Командлет **Get-AzSnapshot** получает свойства снимка.</span><span class="sxs-lookup"><span data-stu-id="caeeb-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="caeeb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="caeeb-107">EXAMPLES</span></span>

### <span data-ttu-id="caeeb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="caeeb-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="caeeb-109">Эта команда получает свойства всех снимков подписки.</span><span class="sxs-lookup"><span data-stu-id="caeeb-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="caeeb-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="caeeb-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="caeeb-111">Эта команда получает свойства всех моментальных снимков в группе ресурсов с именем "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="caeeb-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="caeeb-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="caeeb-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="caeeb-113">Эта команда получает свойства моментального снимка "SnapshotName1" в группе ресурсов с именем "ResourceGroupName1"</span><span class="sxs-lookup"><span data-stu-id="caeeb-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="caeeb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="caeeb-114">PARAMETERS</span></span>

### <span data-ttu-id="caeeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caeeb-115">-DefaultProfile</span></span>
<span data-ttu-id="caeeb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caeeb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caeeb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caeeb-117">-ResourceGroupName</span></span>
<span data-ttu-id="caeeb-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="caeeb-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="caeeb-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="caeeb-119">-SnapshotName</span></span>
<span data-ttu-id="caeeb-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="caeeb-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="caeeb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caeeb-121">CommonParameters</span></span>
<span data-ttu-id="caeeb-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="caeeb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caeeb-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caeeb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caeeb-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="caeeb-124">INPUTS</span></span>

### <span data-ttu-id="caeeb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="caeeb-125">System.String</span></span>

## <span data-ttu-id="caeeb-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="caeeb-126">OUTPUTS</span></span>

### <span data-ttu-id="caeeb-127">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="caeeb-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="caeeb-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="caeeb-128">NOTES</span></span>

## <span data-ttu-id="caeeb-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caeeb-129">RELATED LINKS</span></span>

