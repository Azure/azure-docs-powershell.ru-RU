---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076130"
---
# <span data-ttu-id="eab23-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="eab23-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="eab23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eab23-102">SYNOPSIS</span></span>
<span data-ttu-id="eab23-103">Удаляет пространство имен.</span><span class="sxs-lookup"><span data-stu-id="eab23-103">Removes a namespace.</span></span>

## <span data-ttu-id="eab23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eab23-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eab23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eab23-105">DESCRIPTION</span></span>
<span data-ttu-id="eab23-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="eab23-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="eab23-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="eab23-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="eab23-108">Командлет **Remove-AzureSBNamespace** удаляет пространство имен службы для служебной шины.</span><span class="sxs-lookup"><span data-stu-id="eab23-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="eab23-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eab23-109">EXAMPLES</span></span>

## <span data-ttu-id="eab23-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eab23-110">PARAMETERS</span></span>

### <span data-ttu-id="eab23-111">-Force</span><span class="sxs-lookup"><span data-stu-id="eab23-111">-Force</span></span>
<span data-ttu-id="eab23-112">Если включено, удаляет пространство имен без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="eab23-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab23-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eab23-113">-Name</span></span>
<span data-ttu-id="eab23-114">Указывает имя пространства имен, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="eab23-114">Specifies the name of the namespace to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eab23-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eab23-115">-PassThru</span></span>
<span data-ttu-id="eab23-116">Приводит к тому, что операция возвращает значение true, если она выполняется успешно.</span><span class="sxs-lookup"><span data-stu-id="eab23-116">Causes the operation to return true if it succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab23-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="eab23-117">-Profile</span></span>
<span data-ttu-id="eab23-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eab23-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eab23-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eab23-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab23-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eab23-120">-Confirm</span></span>
<span data-ttu-id="eab23-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eab23-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab23-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab23-122">-WhatIf</span></span>
<span data-ttu-id="eab23-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eab23-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eab23-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eab23-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab23-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab23-125">CommonParameters</span></span>
<span data-ttu-id="eab23-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eab23-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab23-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eab23-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab23-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eab23-128">INPUTS</span></span>

## <span data-ttu-id="eab23-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eab23-129">OUTPUTS</span></span>

## <span data-ttu-id="eab23-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="eab23-130">NOTES</span></span>

## <span data-ttu-id="eab23-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eab23-131">RELATED LINKS</span></span>

[<span data-ttu-id="eab23-132">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="eab23-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


