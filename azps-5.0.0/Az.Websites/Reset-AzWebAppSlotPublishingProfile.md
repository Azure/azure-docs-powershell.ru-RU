---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249246"
---
# <span data-ttu-id="02aa0-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="02aa0-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="02aa0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02aa0-102">SYNOPSIS</span></span>

## <span data-ttu-id="02aa0-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02aa0-103">SYNTAX</span></span>

### <span data-ttu-id="02aa0-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="02aa0-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02aa0-105">S2</span><span class="sxs-lookup"><span data-stu-id="02aa0-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02aa0-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02aa0-106">DESCRIPTION</span></span>
<span data-ttu-id="02aa0-107">Командлет **Reset-AzWebAppSlotPublishingProfile** сбрасывает профиль публикации для указанной области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="02aa0-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="02aa0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02aa0-108">EXAMPLES</span></span>

### <span data-ttu-id="02aa0-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02aa0-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="02aa0-110">Эта команда сбрасывает профиль публикации для слота с именем slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="02aa0-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="02aa0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02aa0-111">PARAMETERS</span></span>

### <span data-ttu-id="02aa0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02aa0-112">-DefaultProfile</span></span>
<span data-ttu-id="02aa0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02aa0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02aa0-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02aa0-114">-Name</span></span>
<span data-ttu-id="02aa0-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="02aa0-115">WebApp Name</span></span>

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

### <span data-ttu-id="02aa0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02aa0-116">-ResourceGroupName</span></span>
<span data-ttu-id="02aa0-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="02aa0-117">Resource Group Name</span></span>

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

### <span data-ttu-id="02aa0-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="02aa0-118">-Slot</span></span>
<span data-ttu-id="02aa0-119">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="02aa0-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="02aa0-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="02aa0-120">-WebApp</span></span>
<span data-ttu-id="02aa0-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="02aa0-121">WebApp Object</span></span>

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

### <span data-ttu-id="02aa0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02aa0-122">CommonParameters</span></span>
<span data-ttu-id="02aa0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02aa0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02aa0-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02aa0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02aa0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02aa0-125">INPUTS</span></span>

### <span data-ttu-id="02aa0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="02aa0-126">System.String</span></span>

### <span data-ttu-id="02aa0-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="02aa0-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="02aa0-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02aa0-128">OUTPUTS</span></span>

### <span data-ttu-id="02aa0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="02aa0-129">System.String</span></span>

## <span data-ttu-id="02aa0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="02aa0-130">NOTES</span></span>

## <span data-ttu-id="02aa0-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02aa0-131">RELATED LINKS</span></span>
