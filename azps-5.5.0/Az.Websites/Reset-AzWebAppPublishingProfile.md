---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242888"
---
# <span data-ttu-id="cce7d-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="cce7d-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="cce7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cce7d-102">SYNOPSIS</span></span>

## <span data-ttu-id="cce7d-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cce7d-103">SYNTAX</span></span>

### <span data-ttu-id="cce7d-104">S1</span><span class="sxs-lookup"><span data-stu-id="cce7d-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cce7d-105">S2</span><span class="sxs-lookup"><span data-stu-id="cce7d-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cce7d-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cce7d-106">DESCRIPTION</span></span>
<span data-ttu-id="cce7d-107">С помощью cmdlet **Reset-AzWebAppPublishingProfile** сбрасывается профиль публикации для указанного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cce7d-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="cce7d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cce7d-108">EXAMPLES</span></span>

### <span data-ttu-id="cce7d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cce7d-109">Example 1</span></span>

<span data-ttu-id="cce7d-110">В следующем примере сбрасывается профиль публикации для веб-приложения IpRule, связанного с группой ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cce7d-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="cce7d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cce7d-111">PARAMETERS</span></span>

### <span data-ttu-id="cce7d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce7d-112">-DefaultProfile</span></span>
<span data-ttu-id="cce7d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cce7d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cce7d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cce7d-114">-Name</span></span>
<span data-ttu-id="cce7d-115">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cce7d-115">WebApp Name</span></span>

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

### <span data-ttu-id="cce7d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cce7d-116">-ResourceGroupName</span></span>
<span data-ttu-id="cce7d-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cce7d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="cce7d-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cce7d-118">-WebApp</span></span>
<span data-ttu-id="cce7d-119">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="cce7d-119">WebApp Object</span></span>

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

### <span data-ttu-id="cce7d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce7d-120">CommonParameters</span></span>
<span data-ttu-id="cce7d-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce7d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce7d-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce7d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce7d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cce7d-123">INPUTS</span></span>

### <span data-ttu-id="cce7d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="cce7d-124">System.String</span></span>

### <span data-ttu-id="cce7d-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="cce7d-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cce7d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cce7d-126">OUTPUTS</span></span>

### <span data-ttu-id="cce7d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cce7d-127">System.String</span></span>

## <span data-ttu-id="cce7d-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cce7d-128">NOTES</span></span>

## <span data-ttu-id="cce7d-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cce7d-129">RELATED LINKS</span></span>
