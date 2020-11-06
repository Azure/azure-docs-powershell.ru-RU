---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 948088f99e90af4594e239dc379133955340e1d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565286"
---
# <span data-ttu-id="be672-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="be672-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="be672-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be672-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be672-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be672-103">SYNTAX</span></span>

### <span data-ttu-id="be672-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="be672-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be672-105">S2</span><span class="sxs-lookup"><span data-stu-id="be672-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be672-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be672-106">DESCRIPTION</span></span>
<span data-ttu-id="be672-107">Командлет **Reset-AzureRmWebAppSlotPublishingProfile** сбрасывает профиль публикации для указанной области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="be672-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="be672-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be672-108">EXAMPLES</span></span>

### <span data-ttu-id="be672-109">1:</span><span class="sxs-lookup"><span data-stu-id="be672-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="be672-110">Эта команда сбрасывает профиль публикации для слота с именем slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="be672-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="be672-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be672-111">PARAMETERS</span></span>

### <span data-ttu-id="be672-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be672-112">-DefaultProfile</span></span>
<span data-ttu-id="be672-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be672-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be672-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be672-114">-Name</span></span>
<span data-ttu-id="be672-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="be672-115">WebApp Name</span></span>

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

### <span data-ttu-id="be672-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be672-116">-ResourceGroupName</span></span>
<span data-ttu-id="be672-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="be672-117">Resource Group Name</span></span>

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

### <span data-ttu-id="be672-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="be672-118">-Slot</span></span>
<span data-ttu-id="be672-119">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="be672-119">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be672-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="be672-120">-WebApp</span></span>
<span data-ttu-id="be672-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="be672-121">WebApp Object</span></span>

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

### <span data-ttu-id="be672-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be672-122">CommonParameters</span></span>
<span data-ttu-id="be672-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be672-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be672-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be672-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be672-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be672-125">INPUTS</span></span>

### <span data-ttu-id="be672-126">System. String</span><span class="sxs-lookup"><span data-stu-id="be672-126">System.String</span></span>

### <span data-ttu-id="be672-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="be672-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="be672-128">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be672-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="be672-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be672-129">OUTPUTS</span></span>

### <span data-ttu-id="be672-130">System. String</span><span class="sxs-lookup"><span data-stu-id="be672-130">System.String</span></span>

## <span data-ttu-id="be672-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="be672-131">NOTES</span></span>

## <span data-ttu-id="be672-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be672-132">RELATED LINKS</span></span>
