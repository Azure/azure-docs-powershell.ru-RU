---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076564"
---
# <span data-ttu-id="75f07-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="75f07-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="75f07-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75f07-102">SYNOPSIS</span></span>
<span data-ttu-id="75f07-103">Получает файл параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="75f07-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="75f07-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75f07-104">SYNTAX</span></span>

### <span data-ttu-id="75f07-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75f07-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="75f07-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="75f07-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="75f07-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75f07-107">DESCRIPTION</span></span>
<span data-ttu-id="75f07-108">Командлет **Get-AzureSiteRecoveryVaultSettingsFile** получает файл параметров для хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="75f07-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="75f07-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75f07-109">EXAMPLES</span></span>

### <span data-ttu-id="75f07-110">Пример 1: получение файла параметров для хранилища</span><span class="sxs-lookup"><span data-stu-id="75f07-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="75f07-111">Первая команда получает активное хранилище Azure Site Recovery с именем ContosoVault с помощью командлета **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="75f07-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="75f07-112">Команда сохраняет это хранилище в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="75f07-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="75f07-113">Вторая команда получает файл параметров для хранилища, хранящегося в $Vault.</span><span class="sxs-lookup"><span data-stu-id="75f07-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="75f07-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75f07-114">PARAMETERS</span></span>

### <span data-ttu-id="75f07-115">-Location</span><span class="sxs-lookup"><span data-stu-id="75f07-115">-Location</span></span>
<span data-ttu-id="75f07-116">Указывает географическое расположение, в которое входит хранилище.</span><span class="sxs-lookup"><span data-stu-id="75f07-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75f07-117">-Name</span></span>
<span data-ttu-id="75f07-118">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="75f07-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-119">-Path</span><span class="sxs-lookup"><span data-stu-id="75f07-119">-Path</span></span>
<span data-ttu-id="75f07-120">Задает путь к файлу параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="75f07-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="75f07-121">Чтобы сохранить этот файл на локальном компьютере, скачайте его с портала хранилища сайтов для восстановления сайта после завершения работы команды.</span><span class="sxs-lookup"><span data-stu-id="75f07-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="75f07-122">-Profile</span></span>
<span data-ttu-id="75f07-123">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="75f07-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75f07-124">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75f07-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75f07-125">-Site</span><span class="sxs-lookup"><span data-stu-id="75f07-125">-Site</span></span>
<span data-ttu-id="75f07-126">Указывает сайт, для которого нужно получить файл параметров.</span><span class="sxs-lookup"><span data-stu-id="75f07-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="75f07-127">Чтобы получить объект **сайта** , используйте командлет **Get-AzureSiteRecoverySite** .</span><span class="sxs-lookup"><span data-stu-id="75f07-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-128">-ID сайта</span><span class="sxs-lookup"><span data-stu-id="75f07-128">-SiteId</span></span>
<span data-ttu-id="75f07-129">Указывает идентификатор сайта.</span><span class="sxs-lookup"><span data-stu-id="75f07-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="75f07-130">-SiteName</span></span>
<span data-ttu-id="75f07-131">Указывает имя сайта.</span><span class="sxs-lookup"><span data-stu-id="75f07-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-132">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="75f07-132">-Vault</span></span>
<span data-ttu-id="75f07-133">Указывает хранилище для сайта.</span><span class="sxs-lookup"><span data-stu-id="75f07-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f07-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f07-134">CommonParameters</span></span>
<span data-ttu-id="75f07-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75f07-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f07-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f07-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f07-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75f07-137">INPUTS</span></span>

## <span data-ttu-id="75f07-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75f07-138">OUTPUTS</span></span>

## <span data-ttu-id="75f07-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="75f07-139">NOTES</span></span>

## <span data-ttu-id="75f07-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75f07-140">RELATED LINKS</span></span>

[<span data-ttu-id="75f07-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="75f07-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="75f07-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="75f07-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="75f07-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="75f07-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="75f07-144">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="75f07-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


