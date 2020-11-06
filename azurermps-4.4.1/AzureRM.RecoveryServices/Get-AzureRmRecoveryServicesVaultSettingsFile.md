---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567531"
---
# <span data-ttu-id="ad404-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ad404-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="ad404-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad404-102">SYNOPSIS</span></span>
<span data-ttu-id="ad404-103">Получает файл параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad404-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad404-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad404-104">SYNTAX</span></span>

### <span data-ttu-id="ad404-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="ad404-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad404-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="ad404-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad404-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="ad404-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad404-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad404-108">DESCRIPTION</span></span>
<span data-ttu-id="ad404-109">Командлет **Get-AzureRmRecoveryServicesVaultSettingsFile** получает файл параметров для хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad404-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ad404-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad404-110">EXAMPLES</span></span>

### <span data-ttu-id="ad404-111">Пример 1: регистрация сервера Windows или компьютера DPM для архивации Azure</span><span class="sxs-lookup"><span data-stu-id="ad404-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="ad404-112">Первая команда получает хранилище с именем TestVault и сохраняет его в переменной $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="ad404-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="ad404-113">Вторая команда задает для переменной $CredsPath значение C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="ad404-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="ad404-114">Последняя команда получает файл учетных данных хранилища для $Vault 01 с использованием учетных данных в $CredsPath для резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="ad404-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="ad404-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad404-115">PARAMETERS</span></span>

### <span data-ttu-id="ad404-116">-Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="ad404-116">-Backup</span></span>
<span data-ttu-id="ad404-117">Указывает, что файл учетных данных хранилища применим к службе архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="ad404-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-118">-Path</span><span class="sxs-lookup"><span data-stu-id="ad404-118">-Path</span></span>
<span data-ttu-id="ad404-119">Задает путь к файлу параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad404-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="ad404-120">Вы можете скачать этот файл на портале хранилища Azure Site Recovery и хранить его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ad404-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ad404-121">-SiteFriendlyName</span></span>
<span data-ttu-id="ad404-122">Указывает понятное имя сайта.</span><span class="sxs-lookup"><span data-stu-id="ad404-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="ad404-123">Используйте этот параметр, если вы загружаете учетные данные хранилища для сайта Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ad404-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="ad404-124">-SiteIdentifier</span></span>
<span data-ttu-id="ad404-125">Указывает идентификатор сайта.</span><span class="sxs-lookup"><span data-stu-id="ad404-125">Specifies the site identifier.</span></span>
<span data-ttu-id="ad404-126">Используйте этот параметр, если вы загружаете учетные данные хранилища для сайта Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="ad404-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ad404-127">-SiteRecovery</span></span>
<span data-ttu-id="ad404-128">Указывает, что файл учетных данных хранилища применим к Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad404-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-129">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="ad404-129">-Vault</span></span>
<span data-ttu-id="ad404-130">Указывает объект хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad404-130">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad404-131">-DefaultProfile</span></span>
<span data-ttu-id="ad404-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad404-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad404-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad404-133">CommonParameters</span></span>
<span data-ttu-id="ad404-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad404-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad404-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad404-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad404-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad404-136">INPUTS</span></span>

### <span data-ttu-id="ad404-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="ad404-137">ARSVault</span></span>
<span data-ttu-id="ad404-138">Параметр "хранилище" принимает значение типа "ARSVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ad404-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="ad404-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad404-139">OUTPUTS</span></span>

### <span data-ttu-id="ad404-140">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="ad404-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="ad404-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad404-141">NOTES</span></span>

## <span data-ttu-id="ad404-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad404-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad404-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad404-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ad404-144">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad404-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ad404-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ad404-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


