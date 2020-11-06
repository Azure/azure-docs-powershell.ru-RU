---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567895"
---
# <span data-ttu-id="d661d-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d661d-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="d661d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d661d-102">SYNOPSIS</span></span>
<span data-ttu-id="d661d-103">Импорт файла параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="d661d-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d661d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d661d-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d661d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d661d-105">DESCRIPTION</span></span>
<span data-ttu-id="d661d-106">Командлет **Import-AzureRmSiteRecoveryVaultSettingsFile** импортирует файл параметров хранилища Azure Site Recovery, чтобы настроить контекст хранилища для последующих операций восстановления сайта в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="d661d-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="d661d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d661d-107">EXAMPLES</span></span>

## <span data-ttu-id="d661d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d661d-108">PARAMETERS</span></span>

### <span data-ttu-id="d661d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d661d-109">-DefaultProfile</span></span>
<span data-ttu-id="d661d-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d661d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d661d-111">-Path</span><span class="sxs-lookup"><span data-stu-id="d661d-111">-Path</span></span>
<span data-ttu-id="d661d-112">Задает путь к файлу параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="d661d-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="d661d-113">Этот файл можно скачать на портале хранилища для восстановления сайта и сохранить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d661d-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d661d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d661d-114">CommonParameters</span></span>
<span data-ttu-id="d661d-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d661d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d661d-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d661d-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d661d-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d661d-117">INPUTS</span></span>

### <span data-ttu-id="d661d-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="d661d-118">None</span></span>
<span data-ttu-id="d661d-119">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d661d-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d661d-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d661d-120">OUTPUTS</span></span>

### <span data-ttu-id="d661d-121">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d661d-121">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="d661d-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="d661d-122">NOTES</span></span>

## <span data-ttu-id="d661d-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d661d-123">RELATED LINKS</span></span>

[<span data-ttu-id="d661d-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d661d-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
