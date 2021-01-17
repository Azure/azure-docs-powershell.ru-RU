---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392460"
---
# <span data-ttu-id="6cfbe-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="6cfbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfbe-103">Получает слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="6cfbe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cfbe-104">SYNTAX</span></span>

### <span data-ttu-id="6cfbe-105">S1</span><span class="sxs-lookup"><span data-stu-id="6cfbe-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cfbe-106">S2</span><span class="sxs-lookup"><span data-stu-id="6cfbe-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cfbe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cfbe-107">DESCRIPTION</span></span>
<span data-ttu-id="6cfbe-108">С **помощью cmdlet Get-AzWebAppSlot** можно получить сведения о слоте Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="6cfbe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cfbe-109">EXAMPLES</span></span>

### <span data-ttu-id="6cfbe-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6cfbe-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="6cfbe-111">Эта команда получает слот Slot001 из веб-приложения WebAppStandard, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6cfbe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cfbe-112">PARAMETERS</span></span>

### <span data-ttu-id="6cfbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfbe-113">-DefaultProfile</span></span>
<span data-ttu-id="6cfbe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cfbe-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6cfbe-115">-Name</span></span>
<span data-ttu-id="6cfbe-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="6cfbe-116">WebApp Name</span></span>

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

### <span data-ttu-id="6cfbe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfbe-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cfbe-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6cfbe-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6cfbe-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-119">-Slot</span></span>
<span data-ttu-id="6cfbe-120">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="6cfbe-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfbe-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6cfbe-121">-WebApp</span></span>
<span data-ttu-id="6cfbe-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6cfbe-122">WebApp Object</span></span>

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

### <span data-ttu-id="6cfbe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfbe-123">CommonParameters</span></span>
<span data-ttu-id="6cfbe-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfbe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfbe-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cfbe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfbe-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cfbe-126">INPUTS</span></span>

### <span data-ttu-id="6cfbe-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6cfbe-127">System.String</span></span>

### <span data-ttu-id="6cfbe-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="6cfbe-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6cfbe-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cfbe-129">OUTPUTS</span></span>

### <span data-ttu-id="6cfbe-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="6cfbe-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6cfbe-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cfbe-131">NOTES</span></span>

## <span data-ttu-id="6cfbe-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cfbe-132">RELATED LINKS</span></span>

[<span data-ttu-id="6cfbe-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="6cfbe-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="6cfbe-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="6cfbe-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="6cfbe-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="6cfbe-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cfbe-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="6cfbe-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6cfbe-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
