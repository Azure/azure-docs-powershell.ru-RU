---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075682"
---
# <span data-ttu-id="b690a-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b690a-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="b690a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b690a-102">SYNOPSIS</span></span>
<span data-ttu-id="b690a-103">Включает диагностику приложений на веб-сайте Azure.</span><span class="sxs-lookup"><span data-stu-id="b690a-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="b690a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b690a-104">SYNTAX</span></span>

### <span data-ttu-id="b690a-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b690a-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b690a-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="b690a-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b690a-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="b690a-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b690a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b690a-108">DESCRIPTION</span></span>
<span data-ttu-id="b690a-109">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b690a-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b690a-110">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b690a-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b690a-111">Включает диагностику приложений на веб-сайте Azure и позволяет настраивать хранение журналов в файловой системе или хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="b690a-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="b690a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b690a-112">EXAMPLES</span></span>

### <span data-ttu-id="b690a-113">Пример 1: включение диагностики с помощью файловой системы</span><span class="sxs-lookup"><span data-stu-id="b690a-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="b690a-114">Этот пример включает ведение журнала приложений для файловой системы с подробным уровнем детализации.</span><span class="sxs-lookup"><span data-stu-id="b690a-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="b690a-115">Пример 2: Включение ведения журнала с помощью хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="b690a-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="b690a-116">Этот пример включает ведение журнала приложений с использованием учетной записи хранения с именем Моя учетная запись и уровнем ведения журнала, установленным на сведения.</span><span class="sxs-lookup"><span data-stu-id="b690a-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="b690a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b690a-117">PARAMETERS</span></span>

### <span data-ttu-id="b690a-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="b690a-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-119">-Файл</span><span class="sxs-lookup"><span data-stu-id="b690a-119">-File</span></span>
<span data-ttu-id="b690a-120">Указывает, что вы хотите использовать файловую систему для хранения файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="b690a-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="b690a-121">-LogLevel</span></span>
<span data-ttu-id="b690a-122">Уровень журнала для хранения.</span><span class="sxs-lookup"><span data-stu-id="b690a-122">The log level to store.</span></span>
<span data-ttu-id="b690a-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b690a-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b690a-124">Ошибки</span><span class="sxs-lookup"><span data-stu-id="b690a-124">Error</span></span>
- <span data-ttu-id="b690a-125">Об</span><span class="sxs-lookup"><span data-stu-id="b690a-125">Warning</span></span>
- <span data-ttu-id="b690a-126">Информация</span><span class="sxs-lookup"><span data-stu-id="b690a-126">Information</span></span>
- <span data-ttu-id="b690a-127">Подробный</span><span class="sxs-lookup"><span data-stu-id="b690a-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b690a-128">-Name</span></span>
<span data-ttu-id="b690a-129">Указывает имя веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="b690a-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="b690a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b690a-130">-PassThru</span></span>
<span data-ttu-id="b690a-131">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b690a-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b690a-132">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b690a-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b690a-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="b690a-133">-Profile</span></span>
<span data-ttu-id="b690a-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b690a-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b690a-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b690a-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b690a-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="b690a-136">-Slot</span></span>
<span data-ttu-id="b690a-137">Указывает имя гнезда.</span><span class="sxs-lookup"><span data-stu-id="b690a-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="b690a-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b690a-138">-StorageAccountName</span></span>
<span data-ttu-id="b690a-139">Учетная запись хранения, которая будет использоваться для хранения журналов.</span><span class="sxs-lookup"><span data-stu-id="b690a-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="b690a-140">Если этот элемент не указан, используется CurrentStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="b690a-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="b690a-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="b690a-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="b690a-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b690a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b690a-144">CommonParameters</span></span>
<span data-ttu-id="b690a-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b690a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b690a-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b690a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b690a-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b690a-147">INPUTS</span></span>

## <span data-ttu-id="b690a-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b690a-148">OUTPUTS</span></span>

## <span data-ttu-id="b690a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b690a-149">NOTES</span></span>

## <span data-ttu-id="b690a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b690a-150">RELATED LINKS</span></span>

[<span data-ttu-id="b690a-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="b690a-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="b690a-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b690a-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="b690a-153">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b690a-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b690a-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b690a-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="b690a-155">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b690a-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


