---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907122"
---
# <span data-ttu-id="3304b-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="3304b-101">New-AzsIpPool</span></span>

## <span data-ttu-id="3304b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3304b-102">SYNOPSIS</span></span>
<span data-ttu-id="3304b-103">Создание пула IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="3304b-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="3304b-104">После создания пул IP-адресов нельзя удалить или изменить.</span><span class="sxs-lookup"><span data-stu-id="3304b-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="3304b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3304b-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3304b-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3304b-106">DESCRIPTION</span></span>
<span data-ttu-id="3304b-107">Создание пула IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="3304b-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="3304b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3304b-108">EXAMPLES</span></span>

### <span data-ttu-id="3304b-109">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3304b-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="3304b-110">Создание нового пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3304b-110">Create a new IP pool.</span></span>

## <span data-ttu-id="3304b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3304b-111">PARAMETERS</span></span>

### <span data-ttu-id="3304b-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3304b-112">-AddressPrefix</span></span>
<span data-ttu-id="3304b-113">Префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="3304b-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3304b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3304b-114">-AsJob</span></span>
<span data-ttu-id="3304b-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="3304b-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3304b-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3304b-116">-EndIpAddress</span></span>
<span data-ttu-id="3304b-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3304b-117">The ending IP address.</span></span>

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

### <span data-ttu-id="3304b-118">-Location</span><span class="sxs-lookup"><span data-stu-id="3304b-118">-Location</span></span>
<span data-ttu-id="3304b-119">Область, в которой расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="3304b-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3304b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3304b-120">-Name</span></span>
<span data-ttu-id="3304b-121">Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="3304b-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3304b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3304b-122">-ResourceGroupName</span></span>
<span data-ttu-id="3304b-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3304b-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3304b-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3304b-124">-StartIpAddress</span></span>
<span data-ttu-id="3304b-125">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="3304b-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3304b-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="3304b-126">-Tags</span></span>
<span data-ttu-id="3304b-127">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="3304b-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3304b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3304b-128">-Confirm</span></span>
<span data-ttu-id="3304b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3304b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3304b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3304b-130">-WhatIf</span></span>
<span data-ttu-id="3304b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3304b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3304b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3304b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3304b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3304b-133">CommonParameters</span></span>
<span data-ttu-id="3304b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3304b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3304b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3304b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3304b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3304b-136">INPUTS</span></span>

## <span data-ttu-id="3304b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3304b-137">OUTPUTS</span></span>

### <span data-ttu-id="3304b-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="3304b-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="3304b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3304b-139">NOTES</span></span>

## <span data-ttu-id="3304b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3304b-140">RELATED LINKS</span></span>

