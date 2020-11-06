---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568812"
---
# <span data-ttu-id="80660-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="80660-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="80660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80660-102">SYNOPSIS</span></span>
<span data-ttu-id="80660-103">Получает свойства диска.</span><span class="sxs-lookup"><span data-stu-id="80660-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80660-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80660-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80660-105">DESCRIPTION</span></span>
<span data-ttu-id="80660-106">Командлет **Get-AzureRmDisk** получает свойства диска.</span><span class="sxs-lookup"><span data-stu-id="80660-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="80660-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80660-107">EXAMPLES</span></span>

### <span data-ttu-id="80660-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="80660-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="80660-109">Эта команда получает свойства диска с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="80660-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="80660-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="80660-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="80660-111">Эта команда получает свойства всех дисков в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="80660-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="80660-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="80660-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="80660-113">Эта команда получает свойства всех дисков подписки.</span><span class="sxs-lookup"><span data-stu-id="80660-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="80660-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80660-114">PARAMETERS</span></span>

### <span data-ttu-id="80660-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80660-115">-DefaultProfile</span></span>
<span data-ttu-id="80660-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80660-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80660-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="80660-117">-DiskName</span></span>
<span data-ttu-id="80660-118">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="80660-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="80660-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80660-119">-ResourceGroupName</span></span>
<span data-ttu-id="80660-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80660-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="80660-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80660-121">CommonParameters</span></span>
<span data-ttu-id="80660-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80660-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80660-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80660-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80660-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80660-124">INPUTS</span></span>

### <span data-ttu-id="80660-125">System. String</span><span class="sxs-lookup"><span data-stu-id="80660-125">System.String</span></span>

## <span data-ttu-id="80660-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80660-126">OUTPUTS</span></span>

### <span data-ttu-id="80660-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="80660-127">System.Object</span></span>

## <span data-ttu-id="80660-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="80660-128">NOTES</span></span>

## <span data-ttu-id="80660-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80660-129">RELATED LINKS</span></span>

