---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5bf1e7cb5a043afaaa4b6fd4d5e8f6820c14fbb1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914245"
---
# <span data-ttu-id="0cc97-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0cc97-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="0cc97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0cc97-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc97-103">Получает свойства управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="0cc97-103">Gets the properties of a Managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cc97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0cc97-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc97-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cc97-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc97-106">Командлет **Get-AzureRmDisk** получает свойства управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="0cc97-106">The **Get-AzureRmDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="0cc97-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0cc97-107">EXAMPLES</span></span>

### <span data-ttu-id="0cc97-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0cc97-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="0cc97-109">Эта команда получает свойства диска с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0cc97-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0cc97-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0cc97-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="0cc97-111">Эта команда получает свойства всех дисков в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0cc97-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0cc97-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0cc97-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="0cc97-113">Эта команда получает свойства всех дисков подписки.</span><span class="sxs-lookup"><span data-stu-id="0cc97-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="0cc97-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0cc97-114">PARAMETERS</span></span>

### <span data-ttu-id="0cc97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc97-115">-DefaultProfile</span></span>
<span data-ttu-id="0cc97-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0cc97-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cc97-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0cc97-117">-DiskName</span></span>
<span data-ttu-id="0cc97-118">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="0cc97-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="0cc97-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc97-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cc97-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0cc97-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0cc97-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc97-121">CommonParameters</span></span>
<span data-ttu-id="0cc97-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0cc97-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc97-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc97-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc97-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0cc97-124">INPUTS</span></span>

### <span data-ttu-id="0cc97-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0cc97-125">System.String</span></span>

## <span data-ttu-id="0cc97-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cc97-126">OUTPUTS</span></span>

### <span data-ttu-id="0cc97-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="0cc97-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="0cc97-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0cc97-128">NOTES</span></span>

## <span data-ttu-id="0cc97-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cc97-129">RELATED LINKS</span></span>

