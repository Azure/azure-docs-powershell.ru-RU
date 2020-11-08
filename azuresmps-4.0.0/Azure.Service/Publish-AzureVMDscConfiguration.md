---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075882"
---
# <span data-ttu-id="41d92-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d92-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="41d92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41d92-102">SYNOPSIS</span></span>
<span data-ttu-id="41d92-103">Публикует сценарий конфигурации нужного состояния в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="41d92-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="41d92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41d92-104">SYNTAX</span></span>

### <span data-ttu-id="41d92-105">UploadArchive (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41d92-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41d92-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="41d92-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d92-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41d92-107">DESCRIPTION</span></span>
<span data-ttu-id="41d92-108">Командлет **Publish-AzureVMDscConfiguration** публикует требуемый сценарий конфигурации состояния в хранилище BLOB-объектов Azure, который позже можно применить к виртуальным машинам Azure с помощью командлета **Set-AzureVMDscExtension** .</span><span class="sxs-lookup"><span data-stu-id="41d92-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="41d92-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41d92-109">EXAMPLES</span></span>

### <span data-ttu-id="41d92-110">Пример 1: публикация сценария конфигурации состояния в хранилище BLOB-объектов</span><span class="sxs-lookup"><span data-stu-id="41d92-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="41d92-111">Эта команда создает ZIP-пакет для указанного сценария и зависимых модулей ресурсов и отправляет его в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="41d92-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="41d92-112">Пример 2: публикация сценария конфигурации состояния в локальном файле</span><span class="sxs-lookup"><span data-stu-id="41d92-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="41d92-113">Эта команда создает ZIP-пакет для указанного сценария и зависимых от него модулей ресурсов и сохраняет его в локальном файле .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="41d92-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="41d92-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41d92-114">PARAMETERS</span></span>

### <span data-ttu-id="41d92-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="41d92-115">-AdditionalPath</span></span>
<span data-ttu-id="41d92-116">Указывает массив дополнительных путей.</span><span class="sxs-lookup"><span data-stu-id="41d92-116">Specifies an array of additional paths.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="41d92-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="41d92-118">Задает путь к локальному ZIP-файлу, который этот командлет записывает в архив конфигурации.</span><span class="sxs-lookup"><span data-stu-id="41d92-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="41d92-119">При использовании этого параметра сценарий конфигурации не загружается в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="41d92-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="41d92-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="41d92-121">Указывает путь к данным конфигурации.</span><span class="sxs-lookup"><span data-stu-id="41d92-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="41d92-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="41d92-122">-ConfigurationPath</span></span>
<span data-ttu-id="41d92-123">Задает путь к файлу, содержащему одну или несколько конфигураций.</span><span class="sxs-lookup"><span data-stu-id="41d92-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="41d92-124">Файл может быть сценарием Windows PowerShell (PS1-файлом), модулем (PSM1-файл) или архивным (ZIP-файлом), содержащим набор модулей Windows PowerShell, каждый из которых находится в отдельном каталоге.</span><span class="sxs-lookup"><span data-stu-id="41d92-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-125">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="41d92-125">-ContainerName</span></span>
<span data-ttu-id="41d92-126">Указывает имя контейнера хранилища Azure, в который загружается конфигурация.</span><span class="sxs-lookup"><span data-stu-id="41d92-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-127">-Force</span><span class="sxs-lookup"><span data-stu-id="41d92-127">-Force</span></span>
<span data-ttu-id="41d92-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="41d92-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41d92-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41d92-129">-InformationAction</span></span>
<span data-ttu-id="41d92-130">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="41d92-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41d92-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="41d92-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41d92-132">Продолжал</span><span class="sxs-lookup"><span data-stu-id="41d92-132">Continue</span></span>
- <span data-ttu-id="41d92-133">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="41d92-133">Ignore</span></span>
- <span data-ttu-id="41d92-134">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="41d92-134">Inquire</span></span>
- <span data-ttu-id="41d92-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41d92-135">SilentlyContinue</span></span>
- <span data-ttu-id="41d92-136">Остановить</span><span class="sxs-lookup"><span data-stu-id="41d92-136">Stop</span></span>
- <span data-ttu-id="41d92-137">Рвать</span><span class="sxs-lookup"><span data-stu-id="41d92-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41d92-138">-InformationVariable</span></span>
<span data-ttu-id="41d92-139">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="41d92-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d92-140">-PassThru</span></span>
<span data-ttu-id="41d92-141">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="41d92-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="41d92-142">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="41d92-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41d92-143">-Profile</span><span class="sxs-lookup"><span data-stu-id="41d92-143">-Profile</span></span>
<span data-ttu-id="41d92-144">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="41d92-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41d92-145">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41d92-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41d92-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="41d92-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="41d92-147">Указывает на то, что этот командлет пропускает обнаружение зависимостей.</span><span class="sxs-lookup"><span data-stu-id="41d92-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="41d92-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="41d92-148">-StorageContext</span></span>
<span data-ttu-id="41d92-149">Указывает контекст хранилища Azure, который предоставляет параметры безопасности, используемые для передачи сценария конфигурации в контейнер, заданный параметром *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="41d92-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="41d92-150">Этот контекст предоставляет доступ к контейнеру для записи.</span><span class="sxs-lookup"><span data-stu-id="41d92-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="41d92-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="41d92-152">Указывает суффикс для конечной точки хранилища (например, core.contoso.net).</span><span class="sxs-lookup"><span data-stu-id="41d92-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d92-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41d92-153">-Confirm</span></span>
<span data-ttu-id="41d92-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41d92-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d92-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d92-155">-WhatIf</span></span>
<span data-ttu-id="41d92-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41d92-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d92-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41d92-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d92-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d92-158">CommonParameters</span></span>
<span data-ttu-id="41d92-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41d92-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d92-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d92-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d92-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41d92-161">INPUTS</span></span>

## <span data-ttu-id="41d92-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41d92-162">OUTPUTS</span></span>

## <span data-ttu-id="41d92-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="41d92-163">NOTES</span></span>

## <span data-ttu-id="41d92-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41d92-164">RELATED LINKS</span></span>

[<span data-ttu-id="41d92-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="41d92-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


