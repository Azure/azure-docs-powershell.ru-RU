---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231521"
---
# <span data-ttu-id="36b04-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="36b04-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="36b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b04-102">SYNOPSIS</span></span>
<span data-ttu-id="36b04-103">Проверяет наличие возможных проблем совместимости между системой и службой Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="36b04-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="36b04-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36b04-104">SYNTAX</span></span>

### <span data-ttu-id="36b04-105">PathBased (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36b04-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="36b04-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="36b04-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="36b04-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36b04-107">DESCRIPTION</span></span>
<span data-ttu-id="36b04-108">Командалет **Invoke-AzStorageSyncCompatibilityCheck** проверяет наличие потенциальных проблем совместимости между системой и синхронизацией файлов Azure. Если задан локальный или удаленный путь, выполняется набор проверки системы и пространства имен файлов, которые затем возвращаются все проблемы совместимости.</span><span class="sxs-lookup"><span data-stu-id="36b04-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="36b04-109">Системные проверки.</span><span class="sxs-lookup"><span data-stu-id="36b04-109">System checks:</span></span>
- <span data-ttu-id="36b04-110">Проверка пространства имен файлов совместимости ОС:</span><span class="sxs-lookup"><span data-stu-id="36b04-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="36b04-111">Неподтверченные символы</span><span class="sxs-lookup"><span data-stu-id="36b04-111">Unsupported characters</span></span>
- <span data-ttu-id="36b04-112">Максимальный размер файла</span><span class="sxs-lookup"><span data-stu-id="36b04-112">Maximum file size</span></span>
- <span data-ttu-id="36b04-113">Максимальная длина пути</span><span class="sxs-lookup"><span data-stu-id="36b04-113">Maximum path length</span></span>
- <span data-ttu-id="36b04-114">Максимальная длина файла</span><span class="sxs-lookup"><span data-stu-id="36b04-114">Maximum file length</span></span>
- <span data-ttu-id="36b04-115">Максимальный размер наборов данных</span><span class="sxs-lookup"><span data-stu-id="36b04-115">Maximum dataset size</span></span>
- <span data-ttu-id="36b04-116">Максимальная глубина каталога</span><span class="sxs-lookup"><span data-stu-id="36b04-116">Maximum directory depth</span></span>

## <span data-ttu-id="36b04-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36b04-117">EXAMPLES</span></span>

### <span data-ttu-id="36b04-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36b04-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="36b04-119">Эта команда проверяет совместимость системы, а также файлов и папок в папке C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="36b04-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="36b04-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="36b04-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="36b04-121">Эта команда проверяет совместимость файлов и папок в папках C:\DATA, но не выполняет проверку совместимости системы.</span><span class="sxs-lookup"><span data-stu-id="36b04-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="36b04-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="36b04-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="36b04-123">Эта команда проверяет совместимость системы, а также файлов и папок в папках C:\DATA, а затем экспортирует результаты в C:\results в C:\Results.</span><span class="sxs-lookup"><span data-stu-id="36b04-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="36b04-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36b04-124">PARAMETERS</span></span>

### <span data-ttu-id="36b04-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="36b04-125">-ComputerName</span></span>
<span data-ttu-id="36b04-126">Компьютер, на который вы выполняете эту проверку.</span><span class="sxs-lookup"><span data-stu-id="36b04-126">The computer you are performing this check on.</span></span>

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

### <span data-ttu-id="36b04-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="36b04-127">-Credential</span></span>
<span data-ttu-id="36b04-128">Ваши учетные данные для подавлимой акции.</span><span class="sxs-lookup"><span data-stu-id="36b04-128">Your credentials for the share you are validating.</span></span>

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

### <span data-ttu-id="36b04-129">-Path</span><span class="sxs-lookup"><span data-stu-id="36b04-129">-Path</span></span>
<span data-ttu-id="36b04-130">UNC-путь к подавлиемой акции.</span><span class="sxs-lookup"><span data-stu-id="36b04-130">The UNC path of the share you are validating.</span></span>

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

### <span data-ttu-id="36b04-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="36b04-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="36b04-132">Установите этот флажок, чтобы пропустить проверки пространства имен файлов и выполнять только системные проверки.</span><span class="sxs-lookup"><span data-stu-id="36b04-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

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

### <span data-ttu-id="36b04-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="36b04-133">-SkipSystemChecks</span></span>
<span data-ttu-id="36b04-134">Установите этот флажок, чтобы пропустить системные проверки и выполнять только проверки пространства имен файлов.</span><span class="sxs-lookup"><span data-stu-id="36b04-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="36b04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b04-135">CommonParameters</span></span>
<span data-ttu-id="36b04-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b04-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b04-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b04-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36b04-138">INPUTS</span></span>

### <span data-ttu-id="36b04-139">Нет</span><span class="sxs-lookup"><span data-stu-id="36b04-139">None</span></span>

## <span data-ttu-id="36b04-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36b04-140">OUTPUTS</span></span>

### <span data-ttu-id="36b04-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="36b04-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="36b04-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36b04-142">NOTES</span></span>
* <span data-ttu-id="36b04-143">Ключевые слова: azure, Az, arm, resource, management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="36b04-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="36b04-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36b04-144">RELATED LINKS</span></span>
