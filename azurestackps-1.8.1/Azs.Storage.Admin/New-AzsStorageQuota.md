---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909182"
---
# <span data-ttu-id="0fff6-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="0fff6-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="0fff6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fff6-102">SYNOPSIS</span></span>
<span data-ttu-id="0fff6-103">Создайте новую квоту хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fff6-103">Create a new storage quota.</span></span>

## <span data-ttu-id="0fff6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fff6-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fff6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fff6-105">DESCRIPTION</span></span>
<span data-ttu-id="0fff6-106">Создайте новую квоту хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fff6-106">Create a new storage quota.</span></span>

## <span data-ttu-id="0fff6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fff6-107">EXAMPLES</span></span>

### <span data-ttu-id="0fff6-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="0fff6-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="0fff6-109">Создание новой квоты хранилища с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="0fff6-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="0fff6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fff6-110">PARAMETERS</span></span>

### <span data-ttu-id="0fff6-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fff6-111">-Name</span></span>
<span data-ttu-id="0fff6-112">Имя квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fff6-112">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fff6-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="0fff6-113">-CapacityInGb</span></span>
<span data-ttu-id="0fff6-114">Максимальное емкость (ГБ).</span><span class="sxs-lookup"><span data-stu-id="0fff6-114">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fff6-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="0fff6-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="0fff6-116">Общее количество учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="0fff6-116">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fff6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="0fff6-117">-Location</span></span>
<span data-ttu-id="0fff6-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0fff6-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fff6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fff6-119">-WhatIf</span></span>
<span data-ttu-id="0fff6-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fff6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fff6-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fff6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fff6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fff6-122">-Confirm</span></span>
<span data-ttu-id="0fff6-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fff6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fff6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fff6-124">CommonParameters</span></span>
<span data-ttu-id="0fff6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fff6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fff6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fff6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fff6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fff6-127">INPUTS</span></span>

## <span data-ttu-id="0fff6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fff6-128">OUTPUTS</span></span>

### <span data-ttu-id="0fff6-129">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="0fff6-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="0fff6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fff6-130">NOTES</span></span>

## <span data-ttu-id="0fff6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fff6-131">RELATED LINKS</span></span>
