---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907229"
---
# <span data-ttu-id="57cee-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="57cee-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="57cee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57cee-102">SYNOPSIS</span></span>
<span data-ttu-id="57cee-103">Создайте новую квоту хранилища.</span><span class="sxs-lookup"><span data-stu-id="57cee-103">Create a new storage quota.</span></span>

## <span data-ttu-id="57cee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57cee-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57cee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57cee-105">DESCRIPTION</span></span>
<span data-ttu-id="57cee-106">Создайте новую квоту хранилища.</span><span class="sxs-lookup"><span data-stu-id="57cee-106">Create a new storage quota.</span></span>

## <span data-ttu-id="57cee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57cee-107">EXAMPLES</span></span>

### <span data-ttu-id="57cee-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="57cee-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="57cee-109">Создание новой квоты хранилища с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="57cee-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="57cee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57cee-110">PARAMETERS</span></span>

### <span data-ttu-id="57cee-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="57cee-111">-CapacityInGb</span></span>
<span data-ttu-id="57cee-112">Максимальное емкость (ГБ).</span><span class="sxs-lookup"><span data-stu-id="57cee-112">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="57cee-113">-Location</span><span class="sxs-lookup"><span data-stu-id="57cee-113">-Location</span></span>
<span data-ttu-id="57cee-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="57cee-114">Resource location.</span></span>

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

### <span data-ttu-id="57cee-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57cee-115">-Name</span></span>
<span data-ttu-id="57cee-116">Имя квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="57cee-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="57cee-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="57cee-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="57cee-118">Общее количество учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="57cee-118">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="57cee-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57cee-119">-Confirm</span></span>
<span data-ttu-id="57cee-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57cee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57cee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57cee-121">-WhatIf</span></span>
<span data-ttu-id="57cee-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57cee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57cee-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57cee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57cee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cee-124">CommonParameters</span></span>
<span data-ttu-id="57cee-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57cee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cee-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57cee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cee-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57cee-127">INPUTS</span></span>

## <span data-ttu-id="57cee-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57cee-128">OUTPUTS</span></span>

### <span data-ttu-id="57cee-129">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="57cee-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="57cee-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="57cee-130">NOTES</span></span>

## <span data-ttu-id="57cee-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57cee-131">RELATED LINKS</span></span>

