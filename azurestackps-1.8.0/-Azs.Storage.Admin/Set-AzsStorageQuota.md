---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908273"
---
# <span data-ttu-id="e5b3f-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e5b3f-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="e5b3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b3f-103">Создание или обновление существующей квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="e5b3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5b3f-104">SYNTAX</span></span>

### <span data-ttu-id="e5b3f-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5b3f-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5b3f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b3f-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5b3f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b3f-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5b3f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5b3f-108">DESCRIPTION</span></span>
<span data-ttu-id="e5b3f-109">Создание или обновление существующей квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="e5b3f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5b3f-110">EXAMPLES</span></span>

### <span data-ttu-id="e5b3f-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e5b3f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="e5b3f-112">Обновление существующей квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="e5b3f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5b3f-113">PARAMETERS</span></span>

### <span data-ttu-id="e5b3f-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="e5b3f-114">-CapacityInGb</span></span>
<span data-ttu-id="e5b3f-115">Максимальное емкость (ГБ).</span><span class="sxs-lookup"><span data-stu-id="e5b3f-115">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b3f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b3f-116">-InputObject</span></span>
<span data-ttu-id="e5b3f-117">Posbbily изменил квоту хранилища, возвращенную функцией Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b3f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e5b3f-118">-Location</span></span>
<span data-ttu-id="e5b3f-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-119">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b3f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5b3f-120">-Name</span></span>
<span data-ttu-id="e5b3f-121">Имя квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-121">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b3f-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e5b3f-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="e5b3f-123">Общее количество учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-123">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b3f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5b3f-124">-ResourceId</span></span>
<span data-ttu-id="e5b3f-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b3f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5b3f-126">-Confirm</span></span>
<span data-ttu-id="e5b3f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b3f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b3f-128">-WhatIf</span></span>
<span data-ttu-id="e5b3f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5b3f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5b3f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b3f-131">CommonParameters</span></span>
<span data-ttu-id="e5b3f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5b3f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b3f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5b3f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b3f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5b3f-134">INPUTS</span></span>

## <span data-ttu-id="e5b3f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5b3f-135">OUTPUTS</span></span>

### <span data-ttu-id="e5b3f-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e5b3f-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e5b3f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5b3f-137">NOTES</span></span>

## <span data-ttu-id="e5b3f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5b3f-138">RELATED LINKS</span></span>

