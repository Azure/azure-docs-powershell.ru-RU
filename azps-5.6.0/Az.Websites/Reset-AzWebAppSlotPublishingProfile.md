---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: bdee1c1fdda561d7265b3f6ff52a443238b6d2b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995812"
---
# <span data-ttu-id="4cf4a-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="4cf4a-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="4cf4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf4a-102">SYNOPSIS</span></span>

## <span data-ttu-id="4cf4a-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4cf4a-103">SYNTAX</span></span>

### <span data-ttu-id="4cf4a-104">S1</span><span class="sxs-lookup"><span data-stu-id="4cf4a-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cf4a-105">S2</span><span class="sxs-lookup"><span data-stu-id="4cf4a-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cf4a-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cf4a-106">DESCRIPTION</span></span>
<span data-ttu-id="4cf4a-107">С помощью cmdlet **Reset-AzWebAppSlotPublishingProfile** сбрасывается профиль публикации для указанного слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="4cf4a-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="4cf4a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4cf4a-108">EXAMPLES</span></span>

### <span data-ttu-id="4cf4a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4cf4a-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="4cf4a-110">Эта команда сбрасывает профиль публикации для слота slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="4cf4a-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4cf4a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cf4a-111">PARAMETERS</span></span>

### <span data-ttu-id="4cf4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf4a-112">-DefaultProfile</span></span>
<span data-ttu-id="4cf4a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf4a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cf4a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4cf4a-114">-Name</span></span>
<span data-ttu-id="4cf4a-115">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="4cf4a-115">WebApp Name</span></span>

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

### <span data-ttu-id="4cf4a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf4a-116">-ResourceGroupName</span></span>
<span data-ttu-id="4cf4a-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4cf4a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="4cf4a-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="4cf4a-118">-Slot</span></span>
<span data-ttu-id="4cf4a-119">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="4cf4a-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4cf4a-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4cf4a-120">-WebApp</span></span>
<span data-ttu-id="4cf4a-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="4cf4a-121">WebApp Object</span></span>

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

### <span data-ttu-id="4cf4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf4a-122">CommonParameters</span></span>
<span data-ttu-id="4cf4a-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf4a-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf4a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf4a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cf4a-125">INPUTS</span></span>

### <span data-ttu-id="4cf4a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf4a-126">System.String</span></span>

### <span data-ttu-id="4cf4a-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4cf4a-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4cf4a-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4cf4a-128">OUTPUTS</span></span>

### <span data-ttu-id="4cf4a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf4a-129">System.String</span></span>

## <span data-ttu-id="4cf4a-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4cf4a-130">NOTES</span></span>

## <span data-ttu-id="4cf4a-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cf4a-131">RELATED LINKS</span></span>
