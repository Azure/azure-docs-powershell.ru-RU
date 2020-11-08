---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079294"
---
# <span data-ttu-id="feaaa-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="feaaa-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="feaaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="feaaa-102">SYNOPSIS</span></span>

## <span data-ttu-id="feaaa-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="feaaa-103">SYNTAX</span></span>

### <span data-ttu-id="feaaa-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="feaaa-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feaaa-105">S2</span><span class="sxs-lookup"><span data-stu-id="feaaa-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="feaaa-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="feaaa-106">DESCRIPTION</span></span>
<span data-ttu-id="feaaa-107">Командлет **Reset-AzWebAppSlotPublishingProfile** сбрасывает профиль публикации для указанной области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="feaaa-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="feaaa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="feaaa-108">EXAMPLES</span></span>

### <span data-ttu-id="feaaa-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="feaaa-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="feaaa-110">Эта команда сбрасывает профиль публикации для слота с именем slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="feaaa-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="feaaa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="feaaa-111">PARAMETERS</span></span>

### <span data-ttu-id="feaaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feaaa-112">-DefaultProfile</span></span>
<span data-ttu-id="feaaa-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="feaaa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feaaa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="feaaa-114">-Name</span></span>
<span data-ttu-id="feaaa-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="feaaa-115">WebApp Name</span></span>

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

### <span data-ttu-id="feaaa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feaaa-116">-ResourceGroupName</span></span>
<span data-ttu-id="feaaa-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="feaaa-117">Resource Group Name</span></span>

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

### <span data-ttu-id="feaaa-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="feaaa-118">-Slot</span></span>
<span data-ttu-id="feaaa-119">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="feaaa-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="feaaa-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="feaaa-120">-WebApp</span></span>
<span data-ttu-id="feaaa-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="feaaa-121">WebApp Object</span></span>

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

### <span data-ttu-id="feaaa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feaaa-122">CommonParameters</span></span>
<span data-ttu-id="feaaa-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="feaaa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feaaa-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feaaa-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feaaa-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="feaaa-125">INPUTS</span></span>

### <span data-ttu-id="feaaa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="feaaa-126">System.String</span></span>

### <span data-ttu-id="feaaa-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="feaaa-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="feaaa-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="feaaa-128">OUTPUTS</span></span>

### <span data-ttu-id="feaaa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="feaaa-129">System.String</span></span>

## <span data-ttu-id="feaaa-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="feaaa-130">NOTES</span></span>

## <span data-ttu-id="feaaa-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="feaaa-131">RELATED LINKS</span></span>
