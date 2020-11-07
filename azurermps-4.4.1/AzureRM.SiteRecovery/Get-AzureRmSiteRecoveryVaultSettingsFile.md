---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 242dfd46b179d1e7d55613d938eddf5b691da6c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734513"
---
# <span data-ttu-id="583c1-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="583c1-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="583c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="583c1-102">SYNOPSIS</span></span>
<span data-ttu-id="583c1-103">Получает файл параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="583c1-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="583c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="583c1-104">SYNTAX</span></span>

### <span data-ttu-id="583c1-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="583c1-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="583c1-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="583c1-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="583c1-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="583c1-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="583c1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="583c1-108">DESCRIPTION</span></span>
<span data-ttu-id="583c1-109">Командлет **Get-AzureRmSiteRecoveryVaultSettingsFile** получает файл параметров для хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="583c1-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="583c1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="583c1-110">EXAMPLES</span></span>

## <span data-ttu-id="583c1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="583c1-111">PARAMETERS</span></span>

### <span data-ttu-id="583c1-112">-Path</span><span class="sxs-lookup"><span data-stu-id="583c1-112">-Path</span></span>
<span data-ttu-id="583c1-113">Задает путь к файлу параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="583c1-113">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="583c1-114">Чтобы сохранить этот файл на локальном компьютере, скачайте его на портале восстановления сайта после завершения команды.</span><span class="sxs-lookup"><span data-stu-id="583c1-114">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="583c1-115">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="583c1-115">-SiteFriendlyName</span></span>
<span data-ttu-id="583c1-116">Указывает понятное имя сайта для хранилища, когда сайт является сайтом Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="583c1-116">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="583c1-117">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="583c1-117">-SiteIdentifier</span></span>
<span data-ttu-id="583c1-118">Указывает идентификатор сайта для хранилища, когда сайт является сайтом Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="583c1-118">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="583c1-119">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="583c1-119">-Vault</span></span>
<span data-ttu-id="583c1-120">Указывает объект хранилища для сайта.</span><span class="sxs-lookup"><span data-stu-id="583c1-120">Specifies the vault object for the site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="583c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="583c1-121">-DefaultProfile</span></span>
<span data-ttu-id="583c1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="583c1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="583c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="583c1-123">CommonParameters</span></span>
<span data-ttu-id="583c1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="583c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="583c1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="583c1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="583c1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="583c1-126">INPUTS</span></span>

### <span data-ttu-id="583c1-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="583c1-127">ASRVault</span></span>
<span data-ttu-id="583c1-128">Параметр "хранилище" принимает значение типа "ASRVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="583c1-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="583c1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="583c1-129">OUTPUTS</span></span>

### <span data-ttu-id="583c1-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="583c1-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="583c1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="583c1-131">NOTES</span></span>

## <span data-ttu-id="583c1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="583c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="583c1-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="583c1-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="583c1-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="583c1-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
