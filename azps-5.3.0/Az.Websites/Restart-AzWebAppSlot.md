---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505737"
---
# <span data-ttu-id="0fe07-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="0fe07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fe07-102">SYNOPSIS</span></span>

## <span data-ttu-id="0fe07-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0fe07-103">SYNTAX</span></span>

### <span data-ttu-id="0fe07-104">S1</span><span class="sxs-lookup"><span data-stu-id="0fe07-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe07-105">S2</span><span class="sxs-lookup"><span data-stu-id="0fe07-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe07-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe07-106">DESCRIPTION</span></span>
<span data-ttu-id="0fe07-107">При запуске слота Azure Web App прекращается использование **cmdlet Restart-AzWebAppSlot.**</span><span class="sxs-lookup"><span data-stu-id="0fe07-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="0fe07-108">Если слот веб-приложения остановлен, используйте Start-AzWebAppSlot управления.</span><span class="sxs-lookup"><span data-stu-id="0fe07-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="0fe07-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0fe07-109">EXAMPLES</span></span>

### <span data-ttu-id="0fe07-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0fe07-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="0fe07-111">Эта команда перезапустит слот Slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0fe07-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="0fe07-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fe07-112">PARAMETERS</span></span>

### <span data-ttu-id="0fe07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe07-113">-DefaultProfile</span></span>
<span data-ttu-id="0fe07-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fe07-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0fe07-115">-Name</span></span>
<span data-ttu-id="0fe07-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="0fe07-116">WebApp Name</span></span>

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

### <span data-ttu-id="0fe07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fe07-117">-ResourceGroupName</span></span>
<span data-ttu-id="0fe07-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0fe07-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0fe07-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="0fe07-119">-Slot</span></span>
<span data-ttu-id="0fe07-120">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="0fe07-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0fe07-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0fe07-121">-WebApp</span></span>
<span data-ttu-id="0fe07-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="0fe07-122">WebApp Object</span></span>

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

### <span data-ttu-id="0fe07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe07-123">CommonParameters</span></span>
<span data-ttu-id="0fe07-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe07-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe07-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe07-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fe07-126">INPUTS</span></span>

### <span data-ttu-id="0fe07-127">System.String</span><span class="sxs-lookup"><span data-stu-id="0fe07-127">System.String</span></span>

### <span data-ttu-id="0fe07-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0fe07-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0fe07-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0fe07-129">OUTPUTS</span></span>

### <span data-ttu-id="0fe07-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0fe07-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0fe07-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0fe07-131">NOTES</span></span>

## <span data-ttu-id="0fe07-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fe07-132">RELATED LINKS</span></span>

[<span data-ttu-id="0fe07-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="0fe07-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="0fe07-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="0fe07-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="0fe07-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="0fe07-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0fe07-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="0fe07-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0fe07-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
