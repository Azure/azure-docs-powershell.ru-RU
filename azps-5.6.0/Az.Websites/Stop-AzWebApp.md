---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 102dbd678fe6fe46034a43c46cb713428b8564d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011043"
---
# <span data-ttu-id="99465-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99465-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="99465-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99465-102">SYNOPSIS</span></span>
<span data-ttu-id="99465-103">Остановка Службы Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="99465-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="99465-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99465-104">SYNTAX</span></span>

### <span data-ttu-id="99465-105">S1</span><span class="sxs-lookup"><span data-stu-id="99465-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99465-106">S2</span><span class="sxs-lookup"><span data-stu-id="99465-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99465-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99465-107">DESCRIPTION</span></span>
<span data-ttu-id="99465-108">С **помощью cmdlet Stop-AzWebApp** можно прекратить работу Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="99465-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="99465-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99465-109">EXAMPLES</span></span>

### <span data-ttu-id="99465-110">Пример 1. Остановка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="99465-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="99465-111">Эта команда останавливает веб-приложение ContosoWebApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="99465-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="99465-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99465-112">PARAMETERS</span></span>

### <span data-ttu-id="99465-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99465-113">-DefaultProfile</span></span>
<span data-ttu-id="99465-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99465-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99465-115">-Name</span><span class="sxs-lookup"><span data-stu-id="99465-115">-Name</span></span>
<span data-ttu-id="99465-116">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="99465-116">WebApp Name</span></span>

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

### <span data-ttu-id="99465-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99465-117">-ResourceGroupName</span></span>
<span data-ttu-id="99465-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="99465-118">Resource Group Name</span></span>

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

### <span data-ttu-id="99465-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="99465-119">-WebApp</span></span>
<span data-ttu-id="99465-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="99465-120">WebApp Object</span></span>

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

### <span data-ttu-id="99465-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99465-121">CommonParameters</span></span>
<span data-ttu-id="99465-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99465-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99465-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99465-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99465-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99465-124">INPUTS</span></span>

### <span data-ttu-id="99465-125">System.String</span><span class="sxs-lookup"><span data-stu-id="99465-125">System.String</span></span>

### <span data-ttu-id="99465-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="99465-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="99465-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99465-127">OUTPUTS</span></span>

### <span data-ttu-id="99465-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="99465-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="99465-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99465-129">NOTES</span></span>

## <span data-ttu-id="99465-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99465-130">RELATED LINKS</span></span>

[<span data-ttu-id="99465-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99465-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="99465-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99465-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="99465-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99465-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="99465-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99465-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="99465-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="99465-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


