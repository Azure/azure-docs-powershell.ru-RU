---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243783"
---
# <span data-ttu-id="32aa2-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="32aa2-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="32aa2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="32aa2-103">Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="32aa2-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="32aa2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32aa2-104">SYNTAX</span></span>

### <span data-ttu-id="32aa2-105">PathBased (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32aa2-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="32aa2-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="32aa2-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="32aa2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32aa2-107">DESCRIPTION</span></span>
<span data-ttu-id="32aa2-108">Командлет **Invoke-AzStorageSyncCompatibilityCheck** проверяет наличие потенциальных проблем с совместимостью между вашей системой и синхронизацией файлов Azure. Если указан локальный или удаленный путь, он выполняет набор проверок пространства имен System и File и возвращает все найденные проблемы совместимости.</span><span class="sxs-lookup"><span data-stu-id="32aa2-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="32aa2-109">Проверки системы:</span><span class="sxs-lookup"><span data-stu-id="32aa2-109">System checks:</span></span>
- <span data-ttu-id="32aa2-110">Проверки пространства имен файла совместимости ОС:</span><span class="sxs-lookup"><span data-stu-id="32aa2-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="32aa2-111">Неподдерживаемые символы</span><span class="sxs-lookup"><span data-stu-id="32aa2-111">Unsupported characters</span></span>
- <span data-ttu-id="32aa2-112">Максимальный размер файла</span><span class="sxs-lookup"><span data-stu-id="32aa2-112">Maximum file size</span></span>
- <span data-ttu-id="32aa2-113">Максимальная длина пути</span><span class="sxs-lookup"><span data-stu-id="32aa2-113">Maximum path length</span></span>
- <span data-ttu-id="32aa2-114">Максимальная длина файла</span><span class="sxs-lookup"><span data-stu-id="32aa2-114">Maximum file length</span></span>
- <span data-ttu-id="32aa2-115">Максимальный размер набора данных</span><span class="sxs-lookup"><span data-stu-id="32aa2-115">Maximum dataset size</span></span>
- <span data-ttu-id="32aa2-116">Максимальная глубина каталога</span><span class="sxs-lookup"><span data-stu-id="32aa2-116">Maximum directory depth</span></span>

## <span data-ttu-id="32aa2-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32aa2-117">EXAMPLES</span></span>

### <span data-ttu-id="32aa2-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32aa2-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="32aa2-119">Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="32aa2-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="32aa2-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="32aa2-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="32aa2-121">Эта команда проверяет совместимость файлов и папок в C:\DATA, но не выполняет проверку совместимости системы.</span><span class="sxs-lookup"><span data-stu-id="32aa2-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="32aa2-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="32aa2-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="32aa2-123">Эта команда проверяет совместимость системы и также файлов и папок в C:\DATA, а затем экспортирует результаты в виде CSV-файла для C:\results.</span><span class="sxs-lookup"><span data-stu-id="32aa2-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="32aa2-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32aa2-124">PARAMETERS</span></span>

### <span data-ttu-id="32aa2-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="32aa2-125">-ComputerName</span></span>
<span data-ttu-id="32aa2-126">Компьютер, на котором вы хотите выполнить эту проверку.</span><span class="sxs-lookup"><span data-stu-id="32aa2-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="32aa2-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="32aa2-127">-Credential</span></span>
<span data-ttu-id="32aa2-128">Ваши учетные данные для проверяемого общего доступа.</span><span class="sxs-lookup"><span data-stu-id="32aa2-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="32aa2-129">-Path</span><span class="sxs-lookup"><span data-stu-id="32aa2-129">-Path</span></span>
<span data-ttu-id="32aa2-130">UNC-путь к проверяемому общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="32aa2-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="32aa2-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="32aa2-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="32aa2-132">Установите этот флаг для пропуска проверок пространства имен файлов и только для проверки системы.</span><span class="sxs-lookup"><span data-stu-id="32aa2-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="32aa2-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="32aa2-133">-SkipSystemChecks</span></span>
<span data-ttu-id="32aa2-134">Установите этот флаг для пропуска системных проверок и выполнения только проверок пространства имен файлов.</span><span class="sxs-lookup"><span data-stu-id="32aa2-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="32aa2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32aa2-135">CommonParameters</span></span>
<span data-ttu-id="32aa2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32aa2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32aa2-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32aa2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32aa2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32aa2-138">INPUTS</span></span>

### <span data-ttu-id="32aa2-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="32aa2-139">None</span></span>

## <span data-ttu-id="32aa2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32aa2-140">OUTPUTS</span></span>

### <span data-ttu-id="32aa2-141">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="32aa2-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="32aa2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="32aa2-142">NOTES</span></span>
* <span data-ttu-id="32aa2-143">Ключевые слова: Azure, AZ, ARM, Resource, Management, storagesync, FileSync</span><span class="sxs-lookup"><span data-stu-id="32aa2-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="32aa2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32aa2-144">RELATED LINKS</span></span>
