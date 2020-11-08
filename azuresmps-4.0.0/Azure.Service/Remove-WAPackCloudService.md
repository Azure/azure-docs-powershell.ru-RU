---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077413"
---
# <span data-ttu-id="ef60f-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="ef60f-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="ef60f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef60f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef60f-103">Удаляет объекты облачной службы.</span><span class="sxs-lookup"><span data-stu-id="ef60f-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="ef60f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef60f-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef60f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef60f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef60f-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="ef60f-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="ef60f-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ef60f-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ef60f-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ef60f-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ef60f-109">Командлет **Remove-WAPackCloudService** удаляет объекты облачной службы.</span><span class="sxs-lookup"><span data-stu-id="ef60f-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="ef60f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef60f-110">EXAMPLES</span></span>

### <span data-ttu-id="ef60f-111">Пример 1: удаление облачной службы</span><span class="sxs-lookup"><span data-stu-id="ef60f-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="ef60f-112">Первая команда получает облачную службу с именем ContosoCloudService01 с помощью командлета **Get-WAPackCloudService** , а затем сохраняет этот объект в переменной $CloudService.</span><span class="sxs-lookup"><span data-stu-id="ef60f-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="ef60f-113">Вторая команда удаляет cloudservice, хранящийся в $CloudService.</span><span class="sxs-lookup"><span data-stu-id="ef60f-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="ef60f-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ef60f-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="ef60f-115">Пример 2: удаление облачной службы без подтверждения</span><span class="sxs-lookup"><span data-stu-id="ef60f-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="ef60f-116">Первая команда получает облачную службу с именем ContosoCloudService02 с помощью командлета **Get-WAPackCloudService** , а затем сохраняет этот объект в переменной $CloudService.</span><span class="sxs-lookup"><span data-stu-id="ef60f-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="ef60f-117">Вторая команда удаляет облачную службу, хранящуюся в $CloudService.</span><span class="sxs-lookup"><span data-stu-id="ef60f-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="ef60f-118">Эта команда включает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="ef60f-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="ef60f-119">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ef60f-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ef60f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef60f-120">PARAMETERS</span></span>

### <span data-ttu-id="ef60f-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="ef60f-121">-CloudService</span></span>
<span data-ttu-id="ef60f-122">Указывает объект облачной службы.</span><span class="sxs-lookup"><span data-stu-id="ef60f-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="ef60f-123">Чтобы получить облачную службу, используйте командлет **Get-WAPackCloudService** .</span><span class="sxs-lookup"><span data-stu-id="ef60f-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef60f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ef60f-124">-Force</span></span>
<span data-ttu-id="ef60f-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef60f-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef60f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef60f-126">-PassThru</span></span>
<span data-ttu-id="ef60f-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ef60f-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef60f-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ef60f-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef60f-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef60f-129">-Profile</span></span>
<span data-ttu-id="ef60f-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ef60f-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef60f-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef60f-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef60f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef60f-132">-Confirm</span></span>
<span data-ttu-id="ef60f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef60f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef60f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef60f-134">-WhatIf</span></span>
<span data-ttu-id="ef60f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef60f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef60f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef60f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef60f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef60f-137">CommonParameters</span></span>
<span data-ttu-id="ef60f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef60f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef60f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef60f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef60f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef60f-140">INPUTS</span></span>

## <span data-ttu-id="ef60f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef60f-141">OUTPUTS</span></span>

## <span data-ttu-id="ef60f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef60f-142">NOTES</span></span>

## <span data-ttu-id="ef60f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef60f-143">RELATED LINKS</span></span>

[<span data-ttu-id="ef60f-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="ef60f-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="ef60f-145">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="ef60f-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


