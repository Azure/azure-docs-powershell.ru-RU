---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565572"
---
# <span data-ttu-id="1c71e-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1c71e-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="1c71e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c71e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c71e-103">Получает свойства диска.</span><span class="sxs-lookup"><span data-stu-id="1c71e-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c71e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c71e-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c71e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c71e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c71e-106">Командлет **Get-AzureRmDisk** получает свойства диска.</span><span class="sxs-lookup"><span data-stu-id="1c71e-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="1c71e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c71e-107">EXAMPLES</span></span>

### <span data-ttu-id="1c71e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1c71e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="1c71e-109">Эта команда получает свойства диска с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1c71e-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1c71e-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1c71e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="1c71e-111">Эта команда получает свойства всех дисков в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1c71e-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1c71e-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1c71e-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="1c71e-113">Эта команда получает свойства всех дисков подписки.</span><span class="sxs-lookup"><span data-stu-id="1c71e-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="1c71e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c71e-114">PARAMETERS</span></span>

### <span data-ttu-id="1c71e-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1c71e-115">-DiskName</span></span>
<span data-ttu-id="1c71e-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="1c71e-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="1c71e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c71e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c71e-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c71e-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c71e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c71e-119">CommonParameters</span></span>
<span data-ttu-id="1c71e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c71e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c71e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c71e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c71e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c71e-122">INPUTS</span></span>

### <span data-ttu-id="1c71e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1c71e-123">System.String</span></span>

## <span data-ttu-id="1c71e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c71e-124">OUTPUTS</span></span>

### <span data-ttu-id="1c71e-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="1c71e-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="1c71e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c71e-126">NOTES</span></span>

## <span data-ttu-id="1c71e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c71e-127">RELATED LINKS</span></span>

