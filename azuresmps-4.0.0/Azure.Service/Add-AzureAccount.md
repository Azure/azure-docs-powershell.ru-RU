---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076396"
---
# <span data-ttu-id="8dcb9-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="8dcb9-101">Add-AzureAccount</span></span>

## <span data-ttu-id="8dcb9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="8dcb9-103">Добавление учетной записи Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="8dcb9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dcb9-104">SYNTAX</span></span>

### <span data-ttu-id="8dcb9-105">Пользователь (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dcb9-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8dcb9-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8dcb9-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8dcb9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dcb9-107">DESCRIPTION</span></span>
<span data-ttu-id="8dcb9-108">Командлет **Add-AzureAccount** делает учетную запись Azure и ее подписки доступными в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="8dcb9-109">Это напоминает вход в учетную запись Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="8dcb9-110">Чтобы выйти из учетной записи, используйте командлет **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="8dcb9-111">**Add-AzureAccount** загружает сведения о своей учетной записи Azure и сохраняет ее в файле данных подписки в перемещаемом профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="8dcb9-112">Кроме того, он получает маркер доступа, который позволяет Windows PowerShell получить доступ к учетной записи Azure от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="8dcb9-113">После завершения команды вы можете управлять учетной записью Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="8dcb9-114">Учетную запись Azure можно сделать доступной для Windows PowerShell двумя разными способами.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="8dcb9-115">Вы можете использовать командлет **Add-AzureAccount** , который использует маркеры доступа для проверки подлинности Azure Active Directory (Azure AD) или **Import-AzurePublishSettingsFile** , который использует сертификат управления.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="8dcb9-116">Рекомендации по использованию этого метода приведены [в статье инструкции: подключение к подписке](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="8dcb9-117">При запуске **Add-AzureAccount** открывается интерактивное окно с запросом на вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="8dcb9-118">Этот вход будет действителен, пока не истечет срок действия маркера доступа.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="8dcb9-119">По истечении срока действия командлетов, которым требуется доступ к вашей учетной записи, будет выдать запрос на повторный запуск **надстройки AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="8dcb9-120">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8dcb9-121">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="8dcb9-122">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dcb9-122">EXAMPLES</span></span>

### <span data-ttu-id="8dcb9-123">Пример 1: Добавление учетной записи</span><span class="sxs-lookup"><span data-stu-id="8dcb9-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="8dcb9-124">Эта команда добавляет учетную запись Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="8dcb9-125">При выполнении команды появляется всплывающее окно с запросом имени пользователя и пароля учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="8dcb9-126">Пример 2: использование альтернативного файла данных подписки</span><span class="sxs-lookup"><span data-stu-id="8dcb9-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="8dcb9-127">Эта команда использует параметр **SubscriptionDataFile** для прямого **добавления AzureAccount** для хранения данных учетной записи в C:\Testing\SDF.xml файле вместо файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="8dcb9-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dcb9-128">PARAMETERS</span></span>

### <span data-ttu-id="8dcb9-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="8dcb9-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcb9-130">-Environment</span><span class="sxs-lookup"><span data-stu-id="8dcb9-130">-Environment</span></span>
<span data-ttu-id="8dcb9-131">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="8dcb9-132">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="8dcb9-133">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="8dcb9-134">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcb9-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="8dcb9-135">-Profile</span></span>
<span data-ttu-id="8dcb9-136">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8dcb9-137">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8dcb9-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8dcb9-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcb9-139">-Клиент</span><span class="sxs-lookup"><span data-stu-id="8dcb9-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dcb9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dcb9-140">CommonParameters</span></span>
<span data-ttu-id="8dcb9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dcb9-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dcb9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dcb9-143">INPUTS</span></span>

### <span data-ttu-id="8dcb9-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="8dcb9-144">None</span></span>
<span data-ttu-id="8dcb9-145">Вы не можете передавать входные данные в этот командлет</span><span class="sxs-lookup"><span data-stu-id="8dcb9-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="8dcb9-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dcb9-146">OUTPUTS</span></span>

### <span data-ttu-id="8dcb9-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="8dcb9-147">None</span></span>
<span data-ttu-id="8dcb9-148">Этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="8dcb9-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dcb9-149">NOTES</span></span>
* <span data-ttu-id="8dcb9-150">**Надстройка Add-AzureAccount** (и метод проверки подлинности Azure AD) имеет приоритет над параметрами **Import-AzurePublishSettings** (и способом сертификации управления).</span><span class="sxs-lookup"><span data-stu-id="8dcb9-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="8dcb9-151">Если вы используете команду **Add-AzureAccount** даже один раз в своей учетной записи, используется метод проверки подлинности Azure AD, и сертификат управления пропускается.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="8dcb9-152">Чтобы удалить маркер Azure AD и восстановить метод сертификата управления, используйте командлет **Remove-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="8dcb9-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="8dcb9-153">Для получения дополнительных сведений введите: **Get-Help Remove-AzureAccount**.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="8dcb9-154">Ошибка "срок действия ваших учетных данных истек.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="8dcb9-155">Для повторного входа используйте Add-AzureAccount.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="8dcb9-156">срок действия маркера доступа истек, и Windows PowerShell не может получить доступ к учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="8dcb9-157">Чтобы восстановить доступ к учетной записи, запустите **надстройку Add-AzureAccount** еще раз.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="8dcb9-158">Учетная запись и командлеты подписки Azure PowerShell получают данные из файла данных подписки, а не из действующей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="8dcb9-159">Если вы изменяете учетную запись или подписки за пределами Windows PowerShell, например с помощью портала управления Azure, запустите **Add-AzureAccount** еще раз, чтобы обновить файл данных подписки.</span><span class="sxs-lookup"><span data-stu-id="8dcb9-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="8dcb9-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dcb9-160">RELATED LINKS</span></span>

[<span data-ttu-id="8dcb9-161">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="8dcb9-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="8dcb9-162">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="8dcb9-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="8dcb9-163">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8dcb9-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="8dcb9-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="8dcb9-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="8dcb9-165">Remove-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="8dcb9-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


