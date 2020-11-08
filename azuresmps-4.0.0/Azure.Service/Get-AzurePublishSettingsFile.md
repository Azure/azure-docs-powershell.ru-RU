---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075633"
---
# <span data-ttu-id="a4054-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a4054-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="a4054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4054-102">SYNOPSIS</span></span>
<span data-ttu-id="a4054-103">Загружает файл параметров публикации для подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a4054-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="a4054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4054-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4054-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4054-105">DESCRIPTION</span></span>
<span data-ttu-id="a4054-106">Командлет **Get-AzurePublishSettingsFile** загружает файл параметров публикации для подписки в своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a4054-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="a4054-107">После завершения команды можно использовать командлет **Import-PublishSettingsFile** , чтобы сделать параметры в файле доступными для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4054-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="a4054-108">Чтобы сделать свою учетную запись Azure доступной для Windows PowerShell, вы можете использовать файл параметров публикации или командлет **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="a4054-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="a4054-109">Файлы параметров публикации позволяют заранее подготовить сеанс, чтобы можно было выполнять сценарии и фоновые задания без сопровождения.</span><span class="sxs-lookup"><span data-stu-id="a4054-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="a4054-110">Однако не все службы поддерживают файлы параметров публикации.</span><span class="sxs-lookup"><span data-stu-id="a4054-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="a4054-111">Например, модуль **AzureResourceManager** не поддерживает файлы параметров публикации.</span><span class="sxs-lookup"><span data-stu-id="a4054-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="a4054-112">При запуске **Get-AzurePublishSettingsFile** открывается браузер по умолчанию и появляется запрос на вход в учетную запись Azure, выберите подписку и укажите расположение файловой системы для файла параметров публикации.</span><span class="sxs-lookup"><span data-stu-id="a4054-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="a4054-113">После этого файл параметров публикации для вашей подписки загружается в выбранный файл.</span><span class="sxs-lookup"><span data-stu-id="a4054-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="a4054-114">Файл параметров публикации — это XML-файл с расширением имени файла. publishsettings.</span><span class="sxs-lookup"><span data-stu-id="a4054-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="a4054-115">Файл содержит закодированный сертификат, который предоставляет учетные данные для управления подписками Azure.</span><span class="sxs-lookup"><span data-stu-id="a4054-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="a4054-116">**Примечание о безопасности:** Файлы параметров публикации содержат учетные данные, которые используются для управления подписками и службами Azure.</span><span class="sxs-lookup"><span data-stu-id="a4054-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="a4054-117">Пользователи, которые имеют доступ к файлу параметров публикации, могут редактировать, создавать и удалять службы Azure.</span><span class="sxs-lookup"><span data-stu-id="a4054-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="a4054-118">По соображениям безопасности сохраните файл в папке "Скачанные файлы" или "документы", а затем удалите ее после использования командлета **Import-AzurePublishSettingsFile** для импорта параметров.</span><span class="sxs-lookup"><span data-stu-id="a4054-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="a4054-119">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4054-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a4054-120">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a4054-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="a4054-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4054-121">EXAMPLES</span></span>

### <span data-ttu-id="a4054-122">Пример 1: Загрузка файла параметров публикации</span><span class="sxs-lookup"><span data-stu-id="a4054-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="a4054-123">Эта команда открывает браузер по умолчанию, подключается к вашей учетной записи Windows Azure и загружает файл publishsettings для своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a4054-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="a4054-124">Пример 2: указание сферы</span><span class="sxs-lookup"><span data-stu-id="a4054-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="a4054-125">Эта команда загружает файл параметров публикации для учетной записи в домене contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a4054-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="a4054-126">Используйте команду с параметром **realm** при входе в Azure с помощью учетной записи организации вместо учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a4054-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="a4054-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4054-127">PARAMETERS</span></span>

### <span data-ttu-id="a4054-128">-Environment</span><span class="sxs-lookup"><span data-stu-id="a4054-128">-Environment</span></span>
<span data-ttu-id="a4054-129">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="a4054-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="a4054-130">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="a4054-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="a4054-131">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="a4054-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="a4054-132">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a4054-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="a4054-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4054-133">-PassThru</span></span>
<span data-ttu-id="a4054-134">Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.</span><span class="sxs-lookup"><span data-stu-id="a4054-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="a4054-135">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a4054-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4054-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="a4054-136">-Profile</span></span>
<span data-ttu-id="a4054-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4054-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a4054-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4054-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a4054-139">-Realm</span><span class="sxs-lookup"><span data-stu-id="a4054-139">-Realm</span></span>
<span data-ttu-id="a4054-140">Определяет организацию в ИДЕНТИФИКАТОРе Организации.</span><span class="sxs-lookup"><span data-stu-id="a4054-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="a4054-141">Например, если вы входите в Azure как admin@contoso.com , значение параметра **Realm** — contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a4054-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="a4054-142">Используйте этот параметр, если вы используете идентификатор организации для входа на портал Azure.</span><span class="sxs-lookup"><span data-stu-id="a4054-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="a4054-143">Этот параметр не требуется при использовании учетной записи Майкрософт, например учетной записи outlook.com или live.com.</span><span class="sxs-lookup"><span data-stu-id="a4054-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="a4054-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4054-144">CommonParameters</span></span>
<span data-ttu-id="a4054-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4054-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4054-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4054-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4054-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4054-147">INPUTS</span></span>

### <span data-ttu-id="a4054-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4054-148">None</span></span>
<span data-ttu-id="a4054-149">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="a4054-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a4054-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4054-150">OUTPUTS</span></span>

### <span data-ttu-id="a4054-151">None и System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4054-151">None or System.Boolean</span></span>
<span data-ttu-id="a4054-152">При использовании параметра *PassThru* этот командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="a4054-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="a4054-153">В противном случае этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a4054-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="a4054-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4054-154">NOTES</span></span>

## <span data-ttu-id="a4054-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4054-155">RELATED LINKS</span></span>

[<span data-ttu-id="a4054-156">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="a4054-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="a4054-157">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a4054-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


