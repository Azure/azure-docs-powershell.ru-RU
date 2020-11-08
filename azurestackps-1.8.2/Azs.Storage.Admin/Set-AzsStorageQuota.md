---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077014"
---
# <span data-ttu-id="d2cd5-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="d2cd5-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="d2cd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cd5-103">Создание или обновление существующей квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="d2cd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2cd5-104">SYNTAX</span></span>

### <span data-ttu-id="d2cd5-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2cd5-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2cd5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2cd5-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2cd5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2cd5-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2cd5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2cd5-108">DESCRIPTION</span></span>
<span data-ttu-id="d2cd5-109">Создание или обновление существующей квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="d2cd5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2cd5-110">EXAMPLES</span></span>

### <span data-ttu-id="d2cd5-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="d2cd5-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="d2cd5-112">Обновление существующей квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="d2cd5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2cd5-113">PARAMETERS</span></span>

### <span data-ttu-id="d2cd5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2cd5-114">-Name</span></span>
<span data-ttu-id="d2cd5-115">Имя квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="d2cd5-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="d2cd5-116">-CapacityInGb</span></span>
<span data-ttu-id="d2cd5-117">Максимальное емкость (ГБ).</span><span class="sxs-lookup"><span data-stu-id="d2cd5-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="d2cd5-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d2cd5-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="d2cd5-119">Общее количество учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="d2cd5-120">-Location</span><span class="sxs-lookup"><span data-stu-id="d2cd5-120">-Location</span></span>
<span data-ttu-id="d2cd5-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-121">Resource location.</span></span>

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

### <span data-ttu-id="d2cd5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2cd5-122">-ResourceId</span></span>
<span data-ttu-id="d2cd5-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-123">The resource id.</span></span>

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

### <span data-ttu-id="d2cd5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2cd5-124">-InputObject</span></span>
<span data-ttu-id="d2cd5-125">Posbbily изменил квоту хранилища, возвращенную функцией Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="d2cd5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2cd5-126">-WhatIf</span></span>
<span data-ttu-id="d2cd5-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2cd5-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2cd5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2cd5-129">-Confirm</span></span>
<span data-ttu-id="d2cd5-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2cd5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cd5-131">CommonParameters</span></span>
<span data-ttu-id="d2cd5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2cd5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cd5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2cd5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cd5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2cd5-134">INPUTS</span></span>

## <span data-ttu-id="d2cd5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2cd5-135">OUTPUTS</span></span>

### <span data-ttu-id="d2cd5-136">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="d2cd5-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="d2cd5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2cd5-137">NOTES</span></span>

## <span data-ttu-id="d2cd5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2cd5-138">RELATED LINKS</span></span>
