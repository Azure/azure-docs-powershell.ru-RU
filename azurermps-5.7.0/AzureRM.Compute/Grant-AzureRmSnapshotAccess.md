---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557556"
---
# <span data-ttu-id="e0e57-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e0e57-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="e0e57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0e57-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e57-103">Предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="e0e57-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0e57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0e57-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0e57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0e57-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e57-106">Командлет **Grant-AzureRmSnapshotAccess** предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="e0e57-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="e0e57-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0e57-107">EXAMPLES</span></span>

### <span data-ttu-id="e0e57-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0e57-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="e0e57-109">Предоставьте доступ на чтение к снимку с именем Snapshot01 в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="e0e57-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="e0e57-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0e57-110">PARAMETERS</span></span>

### <span data-ttu-id="e0e57-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="e0e57-111">-Access</span></span>
<span data-ttu-id="e0e57-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="e0e57-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e57-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="e0e57-113">-DurationInSecond</span></span>
<span data-ttu-id="e0e57-114">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="e0e57-114">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0e57-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e57-115">-ResourceGroupName</span></span>
<span data-ttu-id="e0e57-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0e57-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e0e57-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e0e57-117">-SnapshotName</span></span>
<span data-ttu-id="e0e57-118">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="e0e57-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="e0e57-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0e57-119">-Confirm</span></span>
<span data-ttu-id="e0e57-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0e57-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e57-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e57-121">-WhatIf</span></span>
<span data-ttu-id="e0e57-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0e57-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0e57-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0e57-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e57-124">CommonParameters</span></span>
<span data-ttu-id="e0e57-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0e57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e57-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e57-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e57-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0e57-127">INPUTS</span></span>

### <span data-ttu-id="e0e57-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e0e57-128">System.String</span></span>

## <span data-ttu-id="e0e57-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0e57-129">OUTPUTS</span></span>

### <span data-ttu-id="e0e57-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="e0e57-130">System.Object</span></span>

## <span data-ttu-id="e0e57-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0e57-131">NOTES</span></span>

## <span data-ttu-id="e0e57-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0e57-132">RELATED LINKS</span></span>

