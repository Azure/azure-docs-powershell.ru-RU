---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b71da123933cd190038164b67d37fb81b0d5c973
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003176"
---
# <span data-ttu-id="f5448-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f5448-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="f5448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5448-102">SYNOPSIS</span></span>
<span data-ttu-id="f5448-103">Получает файл параметров хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="f5448-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5448-104">SYNTAX</span></span>

### <span data-ttu-id="f5448-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="f5448-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5448-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="f5448-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5448-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="f5448-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5448-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5448-108">DESCRIPTION</span></span>
<span data-ttu-id="f5448-109">**Cmdlet Get-AzRecoveryServicesVaultSettingsFile** получает файл параметров для хранилища восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f5448-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5448-110">EXAMPLES</span></span>

### <span data-ttu-id="f5448-111">Пример 1. Регистрация компьютера с Windows Server или DPM для резервного копирования Azure</span><span class="sxs-lookup"><span data-stu-id="f5448-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="f5448-112">Первая команда получает хранилище TestVault, а затем сохраняет его в переменной $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="f5448-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="f5448-113">Вторая команда задает переменную $CredsPath C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="f5448-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="f5448-114">Последняя команда получает файл учетных данных хранилища для $Vault 01 с учетными данными в службе $CredsPath для резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="f5448-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f5448-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="f5448-116">Команда получает файл учетных данных хранилища для $Vault 01 типа хранилища siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="f5448-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="f5448-117">Пример 3. Регистрация компьютера с Windows Server или DPM для резервного копирования Azure</span><span class="sxs-lookup"><span data-stu-id="f5448-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="f5448-118">Команда получает файл учетных данных хранилища для $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="f5448-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="f5448-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5448-119">PARAMETERS</span></span>

### <span data-ttu-id="f5448-120">-Backup</span><span class="sxs-lookup"><span data-stu-id="f5448-120">-Backup</span></span>
<span data-ttu-id="f5448-121">Указывает, что файл учетных данных хранилища относится к резервной копии Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="f5448-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="f5448-122">-Certificate</span></span>
<span data-ttu-id="f5448-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="f5448-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="f5448-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5448-124">-DefaultProfile</span></span>
<span data-ttu-id="f5448-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5448-126">-Path</span><span class="sxs-lookup"><span data-stu-id="f5448-126">-Path</span></span>
<span data-ttu-id="f5448-127">Путь к файлу параметров хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="f5448-128">Вы можете скачать этот файл с портала восстановления сайта Azure и сохранить его локально.</span><span class="sxs-lookup"><span data-stu-id="f5448-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="f5448-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f5448-129">-SiteFriendlyName</span></span>
<span data-ttu-id="f5448-130">Указывает имя, которое будет удобно для сайта.</span><span class="sxs-lookup"><span data-stu-id="f5448-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="f5448-131">Используйте этот параметр, если вы скачиваете учетные данные хранилища для Hyper-V сайта.</span><span class="sxs-lookup"><span data-stu-id="f5448-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="f5448-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="f5448-132">-SiteIdentifier</span></span>
<span data-ttu-id="f5448-133">Определяет идентификатор сайта.</span><span class="sxs-lookup"><span data-stu-id="f5448-133">Specifies the site identifier.</span></span>
<span data-ttu-id="f5448-134">Используйте этот параметр, если вы скачиваете учетные данные хранилища для Hyper-V сайта.</span><span class="sxs-lookup"><span data-stu-id="f5448-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="f5448-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f5448-135">-SiteRecovery</span></span>
<span data-ttu-id="f5448-136">Указывает, что файл учетных данных хранилища относится к восстановлению сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="f5448-137">-Vault</span><span class="sxs-lookup"><span data-stu-id="f5448-137">-Vault</span></span>
<span data-ttu-id="f5448-138">Указывает объект хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f5448-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="f5448-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5448-139">CommonParameters</span></span>
<span data-ttu-id="f5448-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5448-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5448-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5448-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5448-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5448-142">INPUTS</span></span>

### <span data-ttu-id="f5448-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="f5448-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f5448-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5448-144">OUTPUTS</span></span>

### <span data-ttu-id="f5448-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="f5448-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="f5448-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5448-146">NOTES</span></span>

## <span data-ttu-id="f5448-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5448-147">RELATED LINKS</span></span>

[<span data-ttu-id="f5448-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f5448-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f5448-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f5448-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="f5448-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f5448-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


