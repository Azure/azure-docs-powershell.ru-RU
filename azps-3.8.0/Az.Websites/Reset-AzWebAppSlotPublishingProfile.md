---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 8670581b376fe185ae4e477524f8f0a01c7cd3a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072916"
---
# <span data-ttu-id="18562-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="18562-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="18562-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18562-102">SYNOPSIS</span></span>

## <span data-ttu-id="18562-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18562-103">SYNTAX</span></span>

### <span data-ttu-id="18562-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="18562-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18562-105">S2</span><span class="sxs-lookup"><span data-stu-id="18562-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18562-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18562-106">DESCRIPTION</span></span>
<span data-ttu-id="18562-107">Командлет **Reset-AzWebAppSlotPublishingProfile** сбрасывает профиль публикации для указанной области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="18562-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="18562-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18562-108">EXAMPLES</span></span>

### <span data-ttu-id="18562-109">1:</span><span class="sxs-lookup"><span data-stu-id="18562-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="18562-110">Эта команда сбрасывает профиль публикации для слота с именем slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="18562-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="18562-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18562-111">PARAMETERS</span></span>

### <span data-ttu-id="18562-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18562-112">-DefaultProfile</span></span>
<span data-ttu-id="18562-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18562-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18562-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18562-114">-Name</span></span>
<span data-ttu-id="18562-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="18562-115">WebApp Name</span></span>

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

### <span data-ttu-id="18562-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18562-116">-ResourceGroupName</span></span>
<span data-ttu-id="18562-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="18562-117">Resource Group Name</span></span>

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

### <span data-ttu-id="18562-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="18562-118">-Slot</span></span>
<span data-ttu-id="18562-119">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="18562-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="18562-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="18562-120">-WebApp</span></span>
<span data-ttu-id="18562-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="18562-121">WebApp Object</span></span>

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

### <span data-ttu-id="18562-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18562-122">CommonParameters</span></span>
<span data-ttu-id="18562-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18562-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18562-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18562-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18562-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18562-125">INPUTS</span></span>

### <span data-ttu-id="18562-126">System. String</span><span class="sxs-lookup"><span data-stu-id="18562-126">System.String</span></span>

### <span data-ttu-id="18562-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="18562-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="18562-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18562-128">OUTPUTS</span></span>

### <span data-ttu-id="18562-129">System. String</span><span class="sxs-lookup"><span data-stu-id="18562-129">System.String</span></span>

## <span data-ttu-id="18562-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="18562-130">NOTES</span></span>

## <span data-ttu-id="18562-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18562-131">RELATED LINKS</span></span>
