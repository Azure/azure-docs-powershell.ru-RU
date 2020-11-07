---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908285"
---
# <span data-ttu-id="acebe-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="acebe-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="acebe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acebe-102">SYNOPSIS</span></span>
<span data-ttu-id="acebe-103">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="acebe-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="acebe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acebe-104">SYNTAX</span></span>

### <span data-ttu-id="acebe-105">Отмена удаления (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acebe-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acebe-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="acebe-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acebe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acebe-107">DESCRIPTION</span></span>
<span data-ttu-id="acebe-108">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="acebe-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="acebe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acebe-109">EXAMPLES</span></span>

### <span data-ttu-id="acebe-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="acebe-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="acebe-111">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="acebe-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="acebe-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acebe-112">PARAMETERS</span></span>

### <span data-ttu-id="acebe-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="acebe-113">-FarmName</span></span>
<span data-ttu-id="acebe-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="acebe-114">Farm Id.</span></span>

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

### <span data-ttu-id="acebe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="acebe-115">-Force</span></span>
<span data-ttu-id="acebe-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="acebe-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="acebe-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="acebe-117">-Name</span></span>
<span data-ttu-id="acebe-118">Внутренний идентификатор учетной записи хранилища, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="acebe-118">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="acebe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acebe-119">-ResourceGroupName</span></span>
<span data-ttu-id="acebe-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acebe-120">Resource group name.</span></span>

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

### <span data-ttu-id="acebe-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acebe-121">-ResourceId</span></span>
<span data-ttu-id="acebe-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="acebe-122">The resource id.</span></span>

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

### <span data-ttu-id="acebe-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acebe-123">-Confirm</span></span>
<span data-ttu-id="acebe-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="acebe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acebe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acebe-125">-WhatIf</span></span>
<span data-ttu-id="acebe-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="acebe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acebe-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="acebe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acebe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acebe-128">CommonParameters</span></span>
<span data-ttu-id="acebe-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acebe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acebe-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acebe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acebe-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acebe-131">INPUTS</span></span>

## <span data-ttu-id="acebe-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acebe-132">OUTPUTS</span></span>

## <span data-ttu-id="acebe-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="acebe-133">NOTES</span></span>

## <span data-ttu-id="acebe-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acebe-134">RELATED LINKS</span></span>

