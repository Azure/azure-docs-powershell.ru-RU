---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 096b062325ddfa12eba1d8c0fe8d6a154c3e77fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565288"
---
# <span data-ttu-id="ad628-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ad628-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="ad628-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad628-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad628-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad628-103">SYNTAX</span></span>

### <span data-ttu-id="ad628-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="ad628-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad628-105">S2</span><span class="sxs-lookup"><span data-stu-id="ad628-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad628-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad628-106">DESCRIPTION</span></span>
<span data-ttu-id="ad628-107">Командлет **Reset-AzureRmWebAppPublishingProfile** сбрасывает профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ad628-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="ad628-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad628-108">EXAMPLES</span></span>

### <span data-ttu-id="ad628-109">1:</span><span class="sxs-lookup"><span data-stu-id="ad628-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="ad628-110">Эта команда сбрасывает профиль публикации для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ad628-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ad628-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad628-111">PARAMETERS</span></span>

### <span data-ttu-id="ad628-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad628-112">-DefaultProfile</span></span>
<span data-ttu-id="ad628-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad628-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad628-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad628-114">-Name</span></span>
<span data-ttu-id="ad628-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ad628-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad628-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad628-116">-ResourceGroupName</span></span>
<span data-ttu-id="ad628-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ad628-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad628-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ad628-118">-WebApp</span></span>
<span data-ttu-id="ad628-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ad628-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad628-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad628-120">CommonParameters</span></span>
<span data-ttu-id="ad628-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad628-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad628-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad628-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad628-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad628-123">INPUTS</span></span>

### <span data-ttu-id="ad628-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ad628-124">System.String</span></span>

### <span data-ttu-id="ad628-125">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ad628-125">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ad628-126">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad628-126">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ad628-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad628-127">OUTPUTS</span></span>

### <span data-ttu-id="ad628-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ad628-128">System.String</span></span>

## <span data-ttu-id="ad628-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad628-129">NOTES</span></span>

## <span data-ttu-id="ad628-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad628-130">RELATED LINKS</span></span>
