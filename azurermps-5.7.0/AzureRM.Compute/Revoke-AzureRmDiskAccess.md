---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568622"
---
# <span data-ttu-id="5e3f2-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5e3f2-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="5e3f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e3f2-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e3f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e3f2-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e3f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e3f2-105">DESCRIPTION</span></span>
<span data-ttu-id="5e3f2-106">Командлет **REVOKE-AzureRmDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="5e3f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e3f2-107">EXAMPLES</span></span>

### <span data-ttu-id="5e3f2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e3f2-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="5e3f2-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="5e3f2-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="5e3f2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e3f2-110">PARAMETERS</span></span>

### <span data-ttu-id="5e3f2-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="5e3f2-111">-DiskName</span></span>
<span data-ttu-id="5e3f2-112">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-112">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e3f2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e3f2-113">-ResourceGroupName</span></span>
<span data-ttu-id="5e3f2-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-114">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e3f2-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e3f2-115">-Confirm</span></span>
<span data-ttu-id="5e3f2-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e3f2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e3f2-117">-WhatIf</span></span>
<span data-ttu-id="5e3f2-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e3f2-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e3f2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e3f2-120">CommonParameters</span></span>
<span data-ttu-id="5e3f2-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e3f2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e3f2-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e3f2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e3f2-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e3f2-123">INPUTS</span></span>

### <span data-ttu-id="5e3f2-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5e3f2-124">System.String</span></span>

## <span data-ttu-id="5e3f2-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e3f2-125">OUTPUTS</span></span>

### <span data-ttu-id="5e3f2-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="5e3f2-126">System.Object</span></span>

## <span data-ttu-id="5e3f2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e3f2-127">NOTES</span></span>

## <span data-ttu-id="5e3f2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e3f2-128">RELATED LINKS</span></span>

