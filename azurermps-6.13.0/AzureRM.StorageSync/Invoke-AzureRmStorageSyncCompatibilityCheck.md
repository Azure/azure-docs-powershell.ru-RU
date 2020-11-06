---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565767"
---
# <span data-ttu-id="96385-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="96385-101">Invoke-AzureRmStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="96385-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96385-102">SYNOPSIS</span></span>
<span data-ttu-id="96385-103">Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="96385-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96385-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96385-104">SYNTAX</span></span>

### <span data-ttu-id="96385-105">PathBased (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96385-105">PathBased (Default)</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### <span data-ttu-id="96385-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="96385-106">ComputerNameBased</span></span>
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## <span data-ttu-id="96385-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96385-107">DESCRIPTION</span></span>
<span data-ttu-id="96385-108">Командлет **Invoke-AzureRmStorageSyncCompatibilityCheck** проверяет наличие потенциальных проблем с совместимостью между вашей системой и синхронизацией файлов Azure. Если указан локальный или удаленный путь, он выполняет набор проверок пространства имен System и File и возвращает все найденные проблемы совместимости.</span><span class="sxs-lookup"><span data-stu-id="96385-108">The **Invoke-AzureRmStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="96385-109">Проверки системы:</span><span class="sxs-lookup"><span data-stu-id="96385-109">System checks:</span></span>
- <span data-ttu-id="96385-110">Проверки пространства имен файла совместимости ОС:</span><span class="sxs-lookup"><span data-stu-id="96385-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="96385-111">Неподдерживаемые символы</span><span class="sxs-lookup"><span data-stu-id="96385-111">Unsupported characters</span></span>
- <span data-ttu-id="96385-112">Максимальный размер файла</span><span class="sxs-lookup"><span data-stu-id="96385-112">Maximum file size</span></span>
- <span data-ttu-id="96385-113">Максимальная длина пути</span><span class="sxs-lookup"><span data-stu-id="96385-113">Maximum path length</span></span>
- <span data-ttu-id="96385-114">Максимальная длина файла</span><span class="sxs-lookup"><span data-stu-id="96385-114">Maximum file length</span></span>
- <span data-ttu-id="96385-115">Максимальный размер набора данных</span><span class="sxs-lookup"><span data-stu-id="96385-115">Maximum dataset size</span></span>
- <span data-ttu-id="96385-116">Максимальная глубина каталога</span><span class="sxs-lookup"><span data-stu-id="96385-116">Maximum directory depth</span></span>

## <span data-ttu-id="96385-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96385-117">EXAMPLES</span></span>

### <span data-ttu-id="96385-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96385-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="96385-119">Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="96385-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="96385-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="96385-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="96385-121">Эта команда проверяет совместимость файлов и папок в C:\DATA, но не выполняет проверку совместимости системы.</span><span class="sxs-lookup"><span data-stu-id="96385-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="96385-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="96385-122">Example 3</span></span>
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

<span data-ttu-id="96385-123">Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA, а затем экспортирует результаты в виде CSV-файла для C:\results.</span><span class="sxs-lookup"><span data-stu-id="96385-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="96385-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96385-124">PARAMETERS</span></span>

### <span data-ttu-id="96385-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="96385-125">-ComputerName</span></span>
<span data-ttu-id="96385-126">Компьютер, на котором вы хотите выполнить эту проверку.</span><span class="sxs-lookup"><span data-stu-id="96385-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96385-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="96385-127">-Credential</span></span>
<span data-ttu-id="96385-128">Ваши учетные данные для проверяемого общего доступа.</span><span class="sxs-lookup"><span data-stu-id="96385-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96385-129">-Path</span><span class="sxs-lookup"><span data-stu-id="96385-129">-Path</span></span>
<span data-ttu-id="96385-130">UNC-путь к проверяемому общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="96385-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96385-131">-Quiet</span><span class="sxs-lookup"><span data-stu-id="96385-131">-Quiet</span></span>
<span data-ttu-id="96385-132">Отключает вывод отчета о выводе на консоль.</span><span class="sxs-lookup"><span data-stu-id="96385-132">Suppresses writing output report to console.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96385-133">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="96385-133">-SkipNamespaceChecks</span></span>
<span data-ttu-id="96385-134">Установите этот флаг для пропуска проверок пространства имен файлов и только для проверки системы.</span><span class="sxs-lookup"><span data-stu-id="96385-134">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96385-135">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="96385-135">-SkipSystemChecks</span></span>
<span data-ttu-id="96385-136">Установите этот флаг для пропуска системных проверок и выполнения только проверок пространства имен файлов.</span><span class="sxs-lookup"><span data-stu-id="96385-136">Set this flag to skip system validations and only perform file namespace validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96385-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96385-137">CommonParameters</span></span>
<span data-ttu-id="96385-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96385-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96385-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96385-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96385-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96385-140">INPUTS</span></span>

### <span data-ttu-id="96385-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="96385-141">None</span></span>

## <span data-ttu-id="96385-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96385-142">OUTPUTS</span></span>

### <span data-ttu-id="96385-143">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="96385-143">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="96385-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="96385-144">NOTES</span></span>
* <span data-ttu-id="96385-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="96385-145">Keywords: azure, azurerm, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="96385-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96385-146">RELATED LINKS</span></span>
