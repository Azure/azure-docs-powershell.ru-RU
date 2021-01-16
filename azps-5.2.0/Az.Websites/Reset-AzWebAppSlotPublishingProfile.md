---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326049"
---
# <span data-ttu-id="50d90-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="50d90-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="50d90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d90-102">SYNOPSIS</span></span>

## <span data-ttu-id="50d90-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50d90-103">SYNTAX</span></span>

### <span data-ttu-id="50d90-104">S1</span><span class="sxs-lookup"><span data-stu-id="50d90-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50d90-105">S2</span><span class="sxs-lookup"><span data-stu-id="50d90-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50d90-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50d90-106">DESCRIPTION</span></span>
<span data-ttu-id="50d90-107">Для указанного слота Web App профиль публикации сбрасывается с помощью cmdlet **Reset-AzWebAppSlotPublishingProfile.**</span><span class="sxs-lookup"><span data-stu-id="50d90-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="50d90-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50d90-108">EXAMPLES</span></span>

### <span data-ttu-id="50d90-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50d90-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="50d90-110">Эта команда сбрасывает профиль публикации для слота slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="50d90-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="50d90-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50d90-111">PARAMETERS</span></span>

### <span data-ttu-id="50d90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d90-112">-DefaultProfile</span></span>
<span data-ttu-id="50d90-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50d90-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50d90-114">-Name</span><span class="sxs-lookup"><span data-stu-id="50d90-114">-Name</span></span>
<span data-ttu-id="50d90-115">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="50d90-115">WebApp Name</span></span>

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

### <span data-ttu-id="50d90-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d90-116">-ResourceGroupName</span></span>
<span data-ttu-id="50d90-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="50d90-117">Resource Group Name</span></span>

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

### <span data-ttu-id="50d90-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="50d90-118">-Slot</span></span>
<span data-ttu-id="50d90-119">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="50d90-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="50d90-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="50d90-120">-WebApp</span></span>
<span data-ttu-id="50d90-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="50d90-121">WebApp Object</span></span>

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

### <span data-ttu-id="50d90-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d90-122">CommonParameters</span></span>
<span data-ttu-id="50d90-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d90-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d90-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d90-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d90-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50d90-125">INPUTS</span></span>

### <span data-ttu-id="50d90-126">System.String</span><span class="sxs-lookup"><span data-stu-id="50d90-126">System.String</span></span>

### <span data-ttu-id="50d90-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="50d90-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="50d90-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50d90-128">OUTPUTS</span></span>

### <span data-ttu-id="50d90-129">System.String</span><span class="sxs-lookup"><span data-stu-id="50d90-129">System.String</span></span>

## <span data-ttu-id="50d90-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50d90-130">NOTES</span></span>

## <span data-ttu-id="50d90-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50d90-131">RELATED LINKS</span></span>