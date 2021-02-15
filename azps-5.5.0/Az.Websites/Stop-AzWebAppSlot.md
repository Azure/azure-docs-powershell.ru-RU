---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231257"
---
# <span data-ttu-id="d328f-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d328f-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="d328f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d328f-102">SYNOPSIS</span></span>
<span data-ttu-id="d328f-103">Остановка слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d328f-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="d328f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d328f-104">SYNTAX</span></span>

### <span data-ttu-id="d328f-105">S1</span><span class="sxs-lookup"><span data-stu-id="d328f-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d328f-106">S2</span><span class="sxs-lookup"><span data-stu-id="d328f-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d328f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d328f-107">DESCRIPTION</span></span>
<span data-ttu-id="d328f-108">С **помощью cmdlet Stop-AzWebAppSlot** можно остановить слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d328f-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="d328f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d328f-109">EXAMPLES</span></span>

### <span data-ttu-id="d328f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d328f-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="d328f-111">Эта команда останавливает слот Slot001, связанный с веб-приложением ContosoWebApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d328f-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="d328f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d328f-112">PARAMETERS</span></span>

### <span data-ttu-id="d328f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d328f-113">-DefaultProfile</span></span>
<span data-ttu-id="d328f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d328f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d328f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d328f-115">-Name</span></span>
<span data-ttu-id="d328f-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="d328f-116">WebApp Name</span></span>

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

### <span data-ttu-id="d328f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d328f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d328f-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d328f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d328f-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="d328f-119">-Slot</span></span>
<span data-ttu-id="d328f-120">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="d328f-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d328f-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d328f-121">-WebApp</span></span>
<span data-ttu-id="d328f-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="d328f-122">WebApp Object</span></span>

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

### <span data-ttu-id="d328f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d328f-123">CommonParameters</span></span>
<span data-ttu-id="d328f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d328f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d328f-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d328f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d328f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d328f-126">INPUTS</span></span>

### <span data-ttu-id="d328f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d328f-127">System.String</span></span>

### <span data-ttu-id="d328f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d328f-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d328f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d328f-129">OUTPUTS</span></span>

### <span data-ttu-id="d328f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d328f-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d328f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d328f-131">NOTES</span></span>

## <span data-ttu-id="d328f-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d328f-132">RELATED LINKS</span></span>
