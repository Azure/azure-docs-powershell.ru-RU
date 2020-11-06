---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556391"
---
# <span data-ttu-id="db7be-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="db7be-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="db7be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db7be-102">SYNOPSIS</span></span>
<span data-ttu-id="db7be-103">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db7be-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="db7be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db7be-104">SYNTAX</span></span>

### <span data-ttu-id="db7be-105">Отмена удаления (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db7be-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7be-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="db7be-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db7be-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db7be-107">DESCRIPTION</span></span>
<span data-ttu-id="db7be-108">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db7be-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="db7be-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db7be-109">EXAMPLES</span></span>

### <span data-ttu-id="db7be-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="db7be-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="db7be-111">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="db7be-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="db7be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db7be-112">PARAMETERS</span></span>

### <span data-ttu-id="db7be-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="db7be-113">-FarmName</span></span>
<span data-ttu-id="db7be-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="db7be-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7be-115">-Force</span><span class="sxs-lookup"><span data-stu-id="db7be-115">-Force</span></span>
<span data-ttu-id="db7be-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="db7be-116">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7be-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db7be-117">-Name</span></span>
<span data-ttu-id="db7be-118">Внутренний идентификатор учетной записи хранилища, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="db7be-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db7be-119">-ResourceGroupName</span></span>
<span data-ttu-id="db7be-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db7be-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7be-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db7be-121">-ResourceId</span></span>
<span data-ttu-id="db7be-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="db7be-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db7be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db7be-123">-Confirm</span></span>
<span data-ttu-id="db7be-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db7be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7be-125">-WhatIf</span></span>
<span data-ttu-id="db7be-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db7be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db7be-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db7be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db7be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7be-128">CommonParameters</span></span>
<span data-ttu-id="db7be-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db7be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7be-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db7be-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7be-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db7be-131">INPUTS</span></span>

## <span data-ttu-id="db7be-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db7be-132">OUTPUTS</span></span>

## <span data-ttu-id="db7be-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="db7be-133">NOTES</span></span>

## <span data-ttu-id="db7be-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db7be-134">RELATED LINKS</span></span>

