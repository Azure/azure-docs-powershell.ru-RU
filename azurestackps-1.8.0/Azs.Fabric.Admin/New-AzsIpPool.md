---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908129"
---
# <span data-ttu-id="7bc65-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="7bc65-101">New-AzsIpPool</span></span>

## <span data-ttu-id="7bc65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bc65-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc65-103">Создание пула IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="7bc65-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="7bc65-104">После создания пул IP-адресов нельзя удалить или изменить.</span><span class="sxs-lookup"><span data-stu-id="7bc65-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="7bc65-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bc65-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bc65-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bc65-106">DESCRIPTION</span></span>
<span data-ttu-id="7bc65-107">Создание пула IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="7bc65-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="7bc65-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bc65-108">EXAMPLES</span></span>

### <span data-ttu-id="7bc65-109">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="7bc65-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="7bc65-110">Создание нового пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="7bc65-110">Create a new IP pool.</span></span>

## <span data-ttu-id="7bc65-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bc65-111">PARAMETERS</span></span>

### <span data-ttu-id="7bc65-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7bc65-112">-Name</span></span>
<span data-ttu-id="7bc65-113">Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="7bc65-113">IP pool name.</span></span>

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

### <span data-ttu-id="7bc65-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7bc65-114">-AddressPrefix</span></span>
<span data-ttu-id="7bc65-115">Префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="7bc65-115">The address prefix.</span></span>

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

### <span data-ttu-id="7bc65-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7bc65-116">-StartIpAddress</span></span>
<span data-ttu-id="7bc65-117">Начальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7bc65-117">The starting IP address.</span></span>

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

### <span data-ttu-id="7bc65-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7bc65-118">-EndIpAddress</span></span>
<span data-ttu-id="7bc65-119">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7bc65-119">The ending IP address.</span></span>

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

### <span data-ttu-id="7bc65-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7bc65-120">-Location</span></span>
<span data-ttu-id="7bc65-121">Область, в которой расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="7bc65-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="7bc65-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc65-122">-ResourceGroupName</span></span>
<span data-ttu-id="7bc65-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7bc65-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="7bc65-124">-Теги</span><span class="sxs-lookup"><span data-stu-id="7bc65-124">-Tags</span></span>
<span data-ttu-id="7bc65-125">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="7bc65-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="7bc65-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7bc65-126">-AsJob</span></span>
<span data-ttu-id="7bc65-127">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="7bc65-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7bc65-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bc65-128">-WhatIf</span></span>
<span data-ttu-id="7bc65-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7bc65-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bc65-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7bc65-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bc65-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bc65-131">-Confirm</span></span>
<span data-ttu-id="7bc65-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7bc65-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bc65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc65-133">CommonParameters</span></span>
<span data-ttu-id="7bc65-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bc65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc65-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc65-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc65-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bc65-136">INPUTS</span></span>

## <span data-ttu-id="7bc65-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bc65-137">OUTPUTS</span></span>

### <span data-ttu-id="7bc65-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="7bc65-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="7bc65-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bc65-139">NOTES</span></span>

## <span data-ttu-id="7bc65-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bc65-140">RELATED LINKS</span></span>
