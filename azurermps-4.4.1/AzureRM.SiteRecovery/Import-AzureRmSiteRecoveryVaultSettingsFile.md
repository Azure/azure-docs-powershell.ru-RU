---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568672"
---
# <span data-ttu-id="0a999-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0a999-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="0a999-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a999-102">SYNOPSIS</span></span>
<span data-ttu-id="0a999-103">Импорт файла параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="0a999-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a999-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a999-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a999-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a999-105">DESCRIPTION</span></span>
<span data-ttu-id="0a999-106">Командлет **Import-AzureRmSiteRecoveryVaultSettingsFile** импортирует файл параметров хранилища Azure Site Recovery, чтобы настроить контекст хранилища для последующих операций восстановления сайта в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="0a999-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="0a999-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a999-107">EXAMPLES</span></span>

## <span data-ttu-id="0a999-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a999-108">PARAMETERS</span></span>

### <span data-ttu-id="0a999-109">-Path</span><span class="sxs-lookup"><span data-stu-id="0a999-109">-Path</span></span>
<span data-ttu-id="0a999-110">Задает путь к файлу параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="0a999-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="0a999-111">Этот файл можно скачать на портале хранилища для восстановления сайта и сохранить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0a999-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a999-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a999-112">-DefaultProfile</span></span>
<span data-ttu-id="0a999-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a999-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a999-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a999-114">CommonParameters</span></span>
<span data-ttu-id="0a999-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a999-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a999-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a999-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a999-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a999-117">INPUTS</span></span>

## <span data-ttu-id="0a999-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a999-118">OUTPUTS</span></span>

### <span data-ttu-id="0a999-119">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0a999-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0a999-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a999-120">NOTES</span></span>

## <span data-ttu-id="0a999-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a999-121">RELATED LINKS</span></span>

[<span data-ttu-id="0a999-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0a999-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
