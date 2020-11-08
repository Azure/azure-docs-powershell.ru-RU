---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076261"
---
# <span data-ttu-id="224d0-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="224d0-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="224d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="224d0-102">SYNOPSIS</span></span>
<span data-ttu-id="224d0-103">Импорт файла параметров публикации, с помощью которого можно управлять учетными записями Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="224d0-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="224d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="224d0-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="224d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="224d0-105">DESCRIPTION</span></span>
<span data-ttu-id="224d0-106">Командлет **Import-AzurePublishSettingsFile** импортирует файл параметров публикации (\*. publishsettings), содержащий сведения об учетных записях Azure, и сохраняет файл данных подписки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="224d0-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="224d0-107">После завершения командлета вы можете управлять учетными записями Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="224d0-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="224d0-108">Перед запуском команды **Import-AzurePublishSettingsFile** запустите **Get-AzurePublishSettingsFile** , который загрузит и сохранит файл параметров публикации, чтобы его можно было импортировать.</span><span class="sxs-lookup"><span data-stu-id="224d0-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="224d0-109">Чтобы сделать свою учетную запись Azure доступной для Windows PowerShell, вы можете использовать файл параметров публикации или командлет **Add-AzureAccount** .</span><span class="sxs-lookup"><span data-stu-id="224d0-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="224d0-110">Файлы параметров публикации позволяют заранее подготовить сеанс, чтобы можно было выполнять сценарии и фоновые задания без сопровождения.</span><span class="sxs-lookup"><span data-stu-id="224d0-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="224d0-111">Однако не все службы поддерживают файлы параметров публикации.</span><span class="sxs-lookup"><span data-stu-id="224d0-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="224d0-112">Например, модуль **AzureResourceManager** не поддерживает файлы параметров публикации.</span><span class="sxs-lookup"><span data-stu-id="224d0-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="224d0-113">**Примечание о безопасности:** Файлы параметров публикации содержат сертификат управления, который закодирован, но не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="224d0-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="224d0-114">Если пользователи могут получить доступ к файлу параметров публикации, они смогут редактировать, создавать и удалять службы Azure.</span><span class="sxs-lookup"><span data-stu-id="224d0-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="224d0-115">По соображениям безопасности сохраните файл в папке "Скачанные файлы" или "документы", а затем удалите ее после использования командлета **Import-AzurePublishSettingsFile** для импорта параметров.</span><span class="sxs-lookup"><span data-stu-id="224d0-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="224d0-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="224d0-116">EXAMPLES</span></span>

### <span data-ttu-id="224d0-117">Пример 1: импорт файла</span><span class="sxs-lookup"><span data-stu-id="224d0-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="224d0-118">Эта команда импортирует файл "C:\Temp\MyAccount.publishsettings".</span><span class="sxs-lookup"><span data-stu-id="224d0-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="224d0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="224d0-119">PARAMETERS</span></span>

### <span data-ttu-id="224d0-120">-Environment</span><span class="sxs-lookup"><span data-stu-id="224d0-120">-Environment</span></span>
<span data-ttu-id="224d0-121">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="224d0-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="224d0-122">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="224d0-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="224d0-123">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="224d0-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="224d0-124">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="224d0-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="224d0-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="224d0-125">-Profile</span></span>
<span data-ttu-id="224d0-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="224d0-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="224d0-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="224d0-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="224d0-128">-PublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="224d0-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="224d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224d0-129">CommonParameters</span></span>
<span data-ttu-id="224d0-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="224d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224d0-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="224d0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224d0-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="224d0-132">INPUTS</span></span>

### <span data-ttu-id="224d0-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="224d0-133">None</span></span>
<span data-ttu-id="224d0-134">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="224d0-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="224d0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="224d0-135">OUTPUTS</span></span>

### <span data-ttu-id="224d0-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="224d0-136">None</span></span>
<span data-ttu-id="224d0-137">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="224d0-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="224d0-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="224d0-138">NOTES</span></span>
* <span data-ttu-id="224d0-139">Файл параметров публикации — это XML-файл с расширением имени файла. publishsettings.</span><span class="sxs-lookup"><span data-stu-id="224d0-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="224d0-140">Файл содержит закодированный сертификат, который предоставляет учетные данные для управления подписками Azure.</span><span class="sxs-lookup"><span data-stu-id="224d0-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="224d0-141">После импорта файла удалите его, чтобы избежать угрозы безопасности.</span><span class="sxs-lookup"><span data-stu-id="224d0-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="224d0-142">Файл данных подписки — это XML-файл, который можно безопасно сохранить на компьютере.</span><span class="sxs-lookup"><span data-stu-id="224d0-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="224d0-143">По умолчанию он сохраняется в перемещаемом профиле пользователя ($home/AppData/Roaming).</span><span class="sxs-lookup"><span data-stu-id="224d0-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="224d0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="224d0-144">RELATED LINKS</span></span>

[<span data-ttu-id="224d0-145">Установка и настройка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="224d0-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="224d0-146">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="224d0-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="224d0-147">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="224d0-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


