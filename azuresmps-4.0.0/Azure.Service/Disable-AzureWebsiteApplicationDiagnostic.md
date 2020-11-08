---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075690"
---
# <span data-ttu-id="7eddc-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7eddc-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="7eddc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7eddc-102">SYNOPSIS</span></span>
<span data-ttu-id="7eddc-103">Отключает диагностику приложений для веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="7eddc-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="7eddc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7eddc-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7eddc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eddc-105">DESCRIPTION</span></span>
<span data-ttu-id="7eddc-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7eddc-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7eddc-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7eddc-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7eddc-108">Отключает диагностику приложений для веб-сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="7eddc-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="7eddc-109">Отключение ведения журналов, настроенных для хранения в файловой системе или Azure.</span><span class="sxs-lookup"><span data-stu-id="7eddc-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="7eddc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7eddc-110">EXAMPLES</span></span>

### <span data-ttu-id="7eddc-111">Пример 1: Отключение файла журнала приложения</span><span class="sxs-lookup"><span data-stu-id="7eddc-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="7eddc-112">В следующем примере отключается ведение журнала приложений в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="7eddc-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="7eddc-113">Пример 2: отключение ведения журнала с помощью хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="7eddc-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="7eddc-114">В следующем примере отключается ведение журнала приложений с помощью хранилища.</span><span class="sxs-lookup"><span data-stu-id="7eddc-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="7eddc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7eddc-115">PARAMETERS</span></span>

### <span data-ttu-id="7eddc-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="7eddc-116">-BlobStorage</span></span>
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

### <span data-ttu-id="7eddc-117">-Файл</span><span class="sxs-lookup"><span data-stu-id="7eddc-117">-File</span></span>
<span data-ttu-id="7eddc-118">Указывает, что вы хотите использовать файловую систему для хранения файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="7eddc-118">Specifies that you want to use the file system to store the log files.</span></span>

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

### <span data-ttu-id="7eddc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7eddc-119">-Name</span></span>
<span data-ttu-id="7eddc-120">Указывает имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="7eddc-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="7eddc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eddc-121">-PassThru</span></span>
<span data-ttu-id="7eddc-122">Флаг, возвращающий значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="7eddc-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="7eddc-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="7eddc-123">-Profile</span></span>
<span data-ttu-id="7eddc-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7eddc-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7eddc-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7eddc-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7eddc-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="7eddc-126">-Slot</span></span>
<span data-ttu-id="7eddc-127">Указывает имя гнезда.</span><span class="sxs-lookup"><span data-stu-id="7eddc-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="7eddc-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="7eddc-128">-TableStorage</span></span>
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

### <span data-ttu-id="7eddc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eddc-129">CommonParameters</span></span>
<span data-ttu-id="7eddc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7eddc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eddc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eddc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eddc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7eddc-132">INPUTS</span></span>

## <span data-ttu-id="7eddc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eddc-133">OUTPUTS</span></span>

## <span data-ttu-id="7eddc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7eddc-134">NOTES</span></span>

## <span data-ttu-id="7eddc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eddc-135">RELATED LINKS</span></span>

[<span data-ttu-id="7eddc-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7eddc-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="7eddc-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7eddc-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="7eddc-138">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7eddc-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="7eddc-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7eddc-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="7eddc-140">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7eddc-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


