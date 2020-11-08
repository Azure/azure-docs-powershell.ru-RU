---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076127"
---
# <span data-ttu-id="353c4-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="353c4-101">Remove-AzureService</span></span>

## <span data-ttu-id="353c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="353c4-102">SYNOPSIS</span></span>
<span data-ttu-id="353c4-103">Удаляет текущую облачную службу.</span><span class="sxs-lookup"><span data-stu-id="353c4-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="353c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="353c4-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="353c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="353c4-105">DESCRIPTION</span></span>
<span data-ttu-id="353c4-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="353c4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="353c4-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="353c4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="353c4-108">Командлет **Remove-AzureService** останавливает и удаляет текущую облачную службу или службу, соответствующую указанной службе и имени подписки.</span><span class="sxs-lookup"><span data-stu-id="353c4-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="353c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="353c4-109">EXAMPLES</span></span>

## <span data-ttu-id="353c4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="353c4-110">PARAMETERS</span></span>

### <span data-ttu-id="353c4-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="353c4-111">-DeleteAll</span></span>
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

### <span data-ttu-id="353c4-112">-Force</span><span class="sxs-lookup"><span data-stu-id="353c4-112">-Force</span></span>
<span data-ttu-id="353c4-113">Удаление службы без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="353c4-113">Removes the service without prompting for confirmation.</span></span>

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

### <span data-ttu-id="353c4-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="353c4-114">-PassThru</span></span>
<span data-ttu-id="353c4-115">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="353c4-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="353c4-116">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="353c4-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="353c4-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="353c4-117">-Profile</span></span>
<span data-ttu-id="353c4-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="353c4-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="353c4-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="353c4-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="353c4-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="353c4-120">-ServiceName</span></span>
<span data-ttu-id="353c4-121">Указывает имя службы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="353c4-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="353c4-122">Если команда запускается из каталога службы, но имя не задано, используется текущее имя службы.</span><span class="sxs-lookup"><span data-stu-id="353c4-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="353c4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="353c4-123">-Confirm</span></span>
<span data-ttu-id="353c4-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="353c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="353c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="353c4-125">-WhatIf</span></span>
<span data-ttu-id="353c4-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="353c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="353c4-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="353c4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="353c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353c4-128">CommonParameters</span></span>
<span data-ttu-id="353c4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="353c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353c4-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353c4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="353c4-131">INPUTS</span></span>

## <span data-ttu-id="353c4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="353c4-132">OUTPUTS</span></span>

## <span data-ttu-id="353c4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="353c4-133">NOTES</span></span>

## <span data-ttu-id="353c4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="353c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="353c4-135">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="353c4-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="353c4-136">Остановить-AzureService</span><span class="sxs-lookup"><span data-stu-id="353c4-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="353c4-137">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="353c4-137">Start-AzureService</span></span>](./Start-AzureService.md)


