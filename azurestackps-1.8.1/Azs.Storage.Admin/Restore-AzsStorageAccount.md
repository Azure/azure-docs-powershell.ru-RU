---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909181"
---
# <span data-ttu-id="25636-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="25636-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="25636-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25636-102">SYNOPSIS</span></span>
<span data-ttu-id="25636-103">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="25636-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="25636-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25636-104">SYNTAX</span></span>

### <span data-ttu-id="25636-105">Отмена удаления (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25636-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25636-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="25636-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25636-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25636-107">DESCRIPTION</span></span>
<span data-ttu-id="25636-108">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="25636-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="25636-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25636-109">EXAMPLES</span></span>

### <span data-ttu-id="25636-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="25636-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="25636-111">Восстановление удаленной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="25636-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="25636-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25636-112">PARAMETERS</span></span>

### <span data-ttu-id="25636-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="25636-113">-FarmName</span></span>
<span data-ttu-id="25636-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="25636-114">Farm Id.</span></span>

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

### <span data-ttu-id="25636-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25636-115">-Name</span></span>
<span data-ttu-id="25636-116">Внутренний идентификатор учетной записи хранилища, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="25636-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="25636-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25636-117">-ResourceGroupName</span></span>
<span data-ttu-id="25636-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25636-118">Resource group name.</span></span>

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

### <span data-ttu-id="25636-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25636-119">-ResourceId</span></span>
<span data-ttu-id="25636-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="25636-120">The resource id.</span></span>

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

### <span data-ttu-id="25636-121">-Force</span><span class="sxs-lookup"><span data-stu-id="25636-121">-Force</span></span>
<span data-ttu-id="25636-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="25636-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="25636-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25636-123">-WhatIf</span></span>
<span data-ttu-id="25636-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25636-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25636-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25636-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25636-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25636-126">-Confirm</span></span>
<span data-ttu-id="25636-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25636-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25636-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25636-128">CommonParameters</span></span>
<span data-ttu-id="25636-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25636-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25636-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25636-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25636-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25636-131">INPUTS</span></span>

## <span data-ttu-id="25636-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25636-132">OUTPUTS</span></span>

## <span data-ttu-id="25636-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="25636-133">NOTES</span></span>

## <span data-ttu-id="25636-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25636-134">RELATED LINKS</span></span>
