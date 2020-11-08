---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: ABC303ED-8712-4958-B871-E95357012277
online version: ''
schema: 2.0.0
ms.openlocfilehash: 706c1dee2bc4bb21a8cf116d15bfa3e53daeed99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076095"
---
# <span data-ttu-id="a96f9-101">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a96f9-101">Remove-AzureSubscription</span></span>

## <span data-ttu-id="a96f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a96f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a96f9-103">Удаляет подписку на Azure из Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a96f9-103">Deletes an Azure subscription from Windows PowerShell.</span></span>

## <span data-ttu-id="a96f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a96f9-104">SYNTAX</span></span>

### <span data-ttu-id="a96f9-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a96f9-105">Name (Default)</span></span>
```
Remove-AzureSubscription -SubscriptionName <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96f9-106">Номер</span><span class="sxs-lookup"><span data-stu-id="a96f9-106">Id</span></span>
```
Remove-AzureSubscription -SubscriptionId <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96f9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a96f9-107">DESCRIPTION</span></span>
<span data-ttu-id="a96f9-108">Командлет **Remove-AzureSubscription** удаляет подписку на Azure из файла данных подписки, поэтому Windows PowerShell не удается ее найти.</span><span class="sxs-lookup"><span data-stu-id="a96f9-108">The **Remove-AzureSubscription** cmdlet deletes an Azure subscription from your subscription data file so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="a96f9-109">Этот командлет не удаляет подписку из Microsoft Azure или может быть изменена в соответствии с реальной подпиской.</span><span class="sxs-lookup"><span data-stu-id="a96f9-109">This cmdlet does not delete the subscription from Microsoft Azure, or change the actual subscription in any way.</span></span>

<span data-ttu-id="a96f9-110">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a96f9-110">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a96f9-111">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a96f9-111">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a96f9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a96f9-112">EXAMPLES</span></span>

### <span data-ttu-id="a96f9-113">Пример 1: Удаление подписки</span><span class="sxs-lookup"><span data-stu-id="a96f9-113">Example 1: Delete a subscription</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test

Confirm
Are you sure you want to perform this action?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="a96f9-114">Эта команда удаляет подписку "тест" из файла данных подписки, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a96f9-114">This command deletes the "Test" subscription from the default subscription data file.</span></span>

### <span data-ttu-id="a96f9-115">Пример 2: удаление из альтернативного файла данных подписки</span><span class="sxs-lookup"><span data-stu-id="a96f9-115">Example 2: Delete from an alternate subscription data file</span></span>
```
C:\PS> Remove-AzureSubscription -SubscriptionName Test -SubscriptionDataFile C:\Subs\MySubscriptions.xml -Force
```

<span data-ttu-id="a96f9-116">Эта команда удаляет тестовую подписку из файла данных подписки MySubscriptions.xml.</span><span class="sxs-lookup"><span data-stu-id="a96f9-116">This command deletes the Test subscription from the MySubscriptions.xml subscription data file.</span></span>
<span data-ttu-id="a96f9-117">В команде параметр *Force* используется для подавления запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a96f9-117">The command uses the *Force* parameter to suppress the confirmation prompt.</span></span>

### <span data-ttu-id="a96f9-118">Пример 3: Удаление подписки в сценарии</span><span class="sxs-lookup"><span data-stu-id="a96f9-118">Example 3: Delete a subscription in a script</span></span>
```
C:\PS> ...if (Remove-AzureSubscription -SubscriptionName Test -PassThru) {...}
```

<span data-ttu-id="a96f9-119">Эта команда использует команду **Remove-AzureSubscription** в инструкции **Если** .</span><span class="sxs-lookup"><span data-stu-id="a96f9-119">This command uses the **Remove-AzureSubscription** command in an **If** statement.</span></span>
<span data-ttu-id="a96f9-120">Он использует параметр *PassThru* , который возвращает логическое значение, чтобы определить, выполняется ли блок сценария в операторе **Если** .</span><span class="sxs-lookup"><span data-stu-id="a96f9-120">It uses the *PassThru* parameter, which returns a Boolean value, to determine whether the script block in the **If** statement is executed.</span></span>

## <span data-ttu-id="a96f9-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a96f9-121">PARAMETERS</span></span>

### <span data-ttu-id="a96f9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a96f9-122">-Force</span></span>
<span data-ttu-id="a96f9-123">Подавляет вывод запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a96f9-123">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="a96f9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a96f9-124">-PassThru</span></span>
<span data-ttu-id="a96f9-125">Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.</span><span class="sxs-lookup"><span data-stu-id="a96f9-125">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="a96f9-126">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a96f9-126">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="a96f9-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="a96f9-127">-Profile</span></span>
<span data-ttu-id="a96f9-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a96f9-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a96f9-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a96f9-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a96f9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a96f9-130">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Id
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96f9-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a96f9-131">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: Name
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96f9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a96f9-132">-Confirm</span></span>
<span data-ttu-id="a96f9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a96f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96f9-134">-WhatIf</span></span>
<span data-ttu-id="a96f9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a96f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96f9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a96f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96f9-137">CommonParameters</span></span>
<span data-ttu-id="a96f9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a96f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96f9-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a96f9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96f9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a96f9-140">INPUTS</span></span>

### <span data-ttu-id="a96f9-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="a96f9-141">None</span></span>
<span data-ttu-id="a96f9-142">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="a96f9-142">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a96f9-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a96f9-143">OUTPUTS</span></span>

### <span data-ttu-id="a96f9-144">None и System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a96f9-144">None or System.Boolean</span></span>
<span data-ttu-id="a96f9-145">Если вы используете параметр *PassThru* , этот командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="a96f9-145">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="a96f9-146">В противном случае он не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a96f9-146">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="a96f9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a96f9-147">NOTES</span></span>

## <span data-ttu-id="a96f9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a96f9-148">RELATED LINKS</span></span>

[<span data-ttu-id="a96f9-149">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a96f9-149">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="a96f9-150">SELECT-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a96f9-150">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)

[<span data-ttu-id="a96f9-151">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a96f9-151">Set-AzureSubscription</span></span>](./Set-AzureSubscription.md)


