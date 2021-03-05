---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: c65eac94a9c44b3b7272116bc0e0757291b121b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011075"
---
# <span data-ttu-id="8ad88-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="8ad88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad88-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad88-103">Запускает слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="8ad88-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="8ad88-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ad88-104">SYNTAX</span></span>

### <span data-ttu-id="8ad88-105">S1</span><span class="sxs-lookup"><span data-stu-id="8ad88-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ad88-106">S2</span><span class="sxs-lookup"><span data-stu-id="8ad88-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ad88-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ad88-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad88-108">Для запуска слота Azure Web App запускается проектлет **Start-AzWebAppSlot.**</span><span class="sxs-lookup"><span data-stu-id="8ad88-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="8ad88-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ad88-109">EXAMPLES</span></span>

### <span data-ttu-id="8ad88-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ad88-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="8ad88-111">Эта команда запускает слот Slot001, связанный с веб-приложением ContosoWebApp, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8ad88-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="8ad88-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ad88-112">PARAMETERS</span></span>

### <span data-ttu-id="8ad88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad88-113">-DefaultProfile</span></span>
<span data-ttu-id="8ad88-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad88-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ad88-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad88-115">-Name</span></span>
<span data-ttu-id="8ad88-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="8ad88-116">WebApp Name</span></span>

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

### <span data-ttu-id="8ad88-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad88-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ad88-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8ad88-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8ad88-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8ad88-119">-Slot</span></span>
<span data-ttu-id="8ad88-120">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="8ad88-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8ad88-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8ad88-121">-WebApp</span></span>
<span data-ttu-id="8ad88-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="8ad88-122">WebApp Object</span></span>

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

### <span data-ttu-id="8ad88-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad88-123">CommonParameters</span></span>
<span data-ttu-id="8ad88-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad88-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad88-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ad88-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad88-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad88-126">INPUTS</span></span>

### <span data-ttu-id="8ad88-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8ad88-127">System.String</span></span>

### <span data-ttu-id="8ad88-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8ad88-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8ad88-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad88-129">OUTPUTS</span></span>

### <span data-ttu-id="8ad88-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8ad88-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8ad88-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ad88-131">NOTES</span></span>

## <span data-ttu-id="8ad88-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ad88-132">RELATED LINKS</span></span>

[<span data-ttu-id="8ad88-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8ad88-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="8ad88-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="8ad88-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="8ad88-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="8ad88-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8ad88-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="8ad88-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8ad88-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
