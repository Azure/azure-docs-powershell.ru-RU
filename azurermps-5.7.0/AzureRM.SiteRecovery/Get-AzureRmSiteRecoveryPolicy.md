---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 80074ff9eb34245a58684bf01157b0b3fadd31e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558796"
---
# <span data-ttu-id="9aa7b-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="9aa7b-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="9aa7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aa7b-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa7b-103">Получает политики защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aa7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aa7b-104">SYNTAX</span></span>

### <span data-ttu-id="9aa7b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9aa7b-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aa7b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9aa7b-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aa7b-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9aa7b-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aa7b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aa7b-108">DESCRIPTION</span></span>
<span data-ttu-id="9aa7b-109">Командлет **Get-AzureRmSiteRecoveryPolicy** получает список настроенных политик защиты для Azure Site Recovery или определенную политику защиты по имени.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="9aa7b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aa7b-110">EXAMPLES</span></span>

## <span data-ttu-id="9aa7b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aa7b-111">PARAMETERS</span></span>

### <span data-ttu-id="9aa7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa7b-112">-DefaultProfile</span></span>
<span data-ttu-id="9aa7b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aa7b-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9aa7b-114">-FriendlyName</span></span>
<span data-ttu-id="9aa7b-115">Указывает понятное имя политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-115">Specifies the friendly name of the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa7b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9aa7b-116">-Name</span></span>
<span data-ttu-id="9aa7b-117">Указывает имя политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-117">Specifies the name of the Site Recovery replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa7b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa7b-118">CommonParameters</span></span>
<span data-ttu-id="9aa7b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa7b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa7b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa7b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aa7b-121">INPUTS</span></span>

### <span data-ttu-id="9aa7b-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="9aa7b-122">None</span></span>
<span data-ttu-id="9aa7b-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9aa7b-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9aa7b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aa7b-124">OUTPUTS</span></span>

### <span data-ttu-id="9aa7b-125">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="9aa7b-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="9aa7b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aa7b-126">NOTES</span></span>

## <span data-ttu-id="9aa7b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aa7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="9aa7b-128">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="9aa7b-128">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="9aa7b-129">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="9aa7b-129">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
