---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077412"
---
# <span data-ttu-id="f4121-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f4121-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="f4121-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4121-102">SYNOPSIS</span></span>
<span data-ttu-id="f4121-103">Удаляет объекты пула статических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f4121-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="f4121-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4121-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f4121-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4121-105">DESCRIPTION</span></span>
<span data-ttu-id="f4121-106">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="f4121-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="f4121-107">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4121-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f4121-108">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f4121-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f4121-109">Командлет **Remove-WAPackStaticIPAddressPool** удаляет статические объекты пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f4121-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="f4121-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4121-110">EXAMPLES</span></span>

### <span data-ttu-id="f4121-111">Пример 1: Удаление статического пула IP-адресов</span><span class="sxs-lookup"><span data-stu-id="f4121-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="f4121-112">Первая команда получает пул статических IP-адресов с именем ContosoStaticIPAddressPool01 с помощью командлета **Get-WAPackStaticIPAddressPool** , а затем сохраняет этот объект в переменной $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f4121-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="f4121-113">Вторая команда удаляет пул статических IP-адресов, хранящийся в $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f4121-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="f4121-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f4121-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="f4121-115">Пример 2: Удаление статического пула IP-адресов без подтверждения</span><span class="sxs-lookup"><span data-stu-id="f4121-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="f4121-116">Первая команда получает статический пул IP-адресов с именем ContosoStaticIPAddressPool02 с помощью командлета **Get-WAPackStaticIPAddressPool** , а затем сохраняет этот объект в переменной $ StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f4121-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="f4121-117">Вторая команда удаляет пул статических IP-адресов, хранящийся в $StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f4121-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="f4121-118">Эта команда включает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="f4121-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="f4121-119">Команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f4121-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f4121-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4121-120">PARAMETERS</span></span>

### <span data-ttu-id="f4121-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f4121-121">-Force</span></span>
<span data-ttu-id="f4121-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4121-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4121-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4121-123">-PassThru</span></span>
<span data-ttu-id="f4121-124">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f4121-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f4121-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f4121-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4121-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="f4121-126">-Profile</span></span>
<span data-ttu-id="f4121-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4121-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f4121-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f4121-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f4121-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f4121-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="f4121-130">Указывает StaticIPAddressPool.</span><span class="sxs-lookup"><span data-stu-id="f4121-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="f4121-131">Для получения пула статических IP-адресов используйте командлет **Get-WAPackStaticIPAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="f4121-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4121-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4121-132">CommonParameters</span></span>
<span data-ttu-id="f4121-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4121-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4121-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4121-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4121-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4121-135">INPUTS</span></span>

## <span data-ttu-id="f4121-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4121-136">OUTPUTS</span></span>

## <span data-ttu-id="f4121-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4121-137">NOTES</span></span>

## <span data-ttu-id="f4121-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4121-138">RELATED LINKS</span></span>

[<span data-ttu-id="f4121-139">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f4121-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="f4121-140">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="f4121-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


