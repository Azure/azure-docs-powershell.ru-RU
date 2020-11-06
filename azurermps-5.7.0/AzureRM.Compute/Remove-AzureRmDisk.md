---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559167"
---
# <span data-ttu-id="f8456-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f8456-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="f8456-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8456-102">SYNOPSIS</span></span>
<span data-ttu-id="f8456-103">Удаление диска.</span><span class="sxs-lookup"><span data-stu-id="f8456-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8456-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8456-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8456-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8456-105">DESCRIPTION</span></span>
<span data-ttu-id="f8456-106">Командлет **Remove-AzureRmDisk** удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="f8456-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="f8456-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8456-107">EXAMPLES</span></span>

### <span data-ttu-id="f8456-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8456-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="f8456-109">Эта команда удаляет диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f8456-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f8456-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8456-110">PARAMETERS</span></span>

### <span data-ttu-id="f8456-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f8456-111">-DiskName</span></span>
<span data-ttu-id="f8456-112">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="f8456-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="f8456-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f8456-113">-Force</span></span>
<span data-ttu-id="f8456-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8456-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8456-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8456-115">-ResourceGroupName</span></span>
<span data-ttu-id="f8456-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8456-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f8456-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8456-117">-Confirm</span></span>
<span data-ttu-id="f8456-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8456-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8456-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8456-119">-WhatIf</span></span>
<span data-ttu-id="f8456-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8456-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8456-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8456-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8456-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8456-122">CommonParameters</span></span>
<span data-ttu-id="f8456-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8456-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8456-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8456-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8456-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8456-125">INPUTS</span></span>

### <span data-ttu-id="f8456-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8456-126">System.String</span></span>

## <span data-ttu-id="f8456-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8456-127">OUTPUTS</span></span>

### <span data-ttu-id="f8456-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="f8456-128">System.Object</span></span>

## <span data-ttu-id="f8456-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8456-129">NOTES</span></span>

## <span data-ttu-id="f8456-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8456-130">RELATED LINKS</span></span>

