---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077691"
---
# <span data-ttu-id="59f96-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="59f96-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="59f96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59f96-102">SYNOPSIS</span></span>
<span data-ttu-id="59f96-103">Получает файл параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="59f96-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="59f96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59f96-104">SYNTAX</span></span>

### <span data-ttu-id="59f96-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="59f96-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59f96-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="59f96-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59f96-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="59f96-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59f96-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59f96-108">DESCRIPTION</span></span>
<span data-ttu-id="59f96-109">Командлет **Get-AzRecoveryServicesVaultSettingsFile** получает файл параметров для хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="59f96-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="59f96-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59f96-110">EXAMPLES</span></span>

### <span data-ttu-id="59f96-111">Пример 1: регистрация сервера Windows или компьютера DPM для архивации Azure</span><span class="sxs-lookup"><span data-stu-id="59f96-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="59f96-112">Первая команда получает хранилище с именем TestVault и сохраняет его в переменной $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="59f96-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="59f96-113">Вторая команда задает для переменной $CredsPath значение C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="59f96-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="59f96-114">Последняя команда получает файл учетных данных хранилища для $Vault 01 с использованием учетных данных в $CredsPath для резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="59f96-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="59f96-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59f96-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="59f96-116">Команда получает файл учетных данных хранилища для $Vault 01 siteRecovery типа хранилища.</span><span class="sxs-lookup"><span data-stu-id="59f96-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="59f96-117">Пример 3: регистрация сервера Windows или компьютера DPM для архивации Azure</span><span class="sxs-lookup"><span data-stu-id="59f96-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="59f96-118">Команда получает файл учетных данных хранилища для $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="59f96-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="59f96-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59f96-119">PARAMETERS</span></span>

### <span data-ttu-id="59f96-120">-Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="59f96-120">-Backup</span></span>
<span data-ttu-id="59f96-121">Указывает, что файл учетных данных хранилища применим к службе архивации Azure.</span><span class="sxs-lookup"><span data-stu-id="59f96-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f96-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="59f96-122">-Certificate</span></span>
<span data-ttu-id="59f96-123">{{Заполнение описания сертификата}}</span><span class="sxs-lookup"><span data-stu-id="59f96-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f96-124">-DefaultProfile</span></span>
<span data-ttu-id="59f96-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59f96-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f96-126">-Path</span><span class="sxs-lookup"><span data-stu-id="59f96-126">-Path</span></span>
<span data-ttu-id="59f96-127">Задает путь к файлу параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="59f96-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="59f96-128">Вы можете скачать этот файл на портале хранилища Azure Site Recovery и хранить его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="59f96-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="59f96-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="59f96-129">-SiteFriendlyName</span></span>
<span data-ttu-id="59f96-130">Указывает понятное имя сайта.</span><span class="sxs-lookup"><span data-stu-id="59f96-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="59f96-131">Используйте этот параметр, если вы загружаете учетные данные хранилища для сайта Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="59f96-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f96-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="59f96-132">-SiteIdentifier</span></span>
<span data-ttu-id="59f96-133">Указывает идентификатор сайта.</span><span class="sxs-lookup"><span data-stu-id="59f96-133">Specifies the site identifier.</span></span>
<span data-ttu-id="59f96-134">Используйте этот параметр, если вы загружаете учетные данные хранилища для сайта Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="59f96-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f96-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="59f96-135">-SiteRecovery</span></span>
<span data-ttu-id="59f96-136">Указывает, что файл учетных данных хранилища применим к Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="59f96-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f96-137">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="59f96-137">-Vault</span></span>
<span data-ttu-id="59f96-138">Указывает объект хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="59f96-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="59f96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f96-139">CommonParameters</span></span>
<span data-ttu-id="59f96-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59f96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f96-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59f96-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f96-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59f96-142">INPUTS</span></span>

### <span data-ttu-id="59f96-143">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="59f96-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="59f96-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59f96-144">OUTPUTS</span></span>

### <span data-ttu-id="59f96-145">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="59f96-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="59f96-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="59f96-146">NOTES</span></span>

## <span data-ttu-id="59f96-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59f96-147">RELATED LINKS</span></span>

[<span data-ttu-id="59f96-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="59f96-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="59f96-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="59f96-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="59f96-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="59f96-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)

