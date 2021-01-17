---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422652"
---
# <span data-ttu-id="c1527-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1527-101">Get-AzWebApp</span></span>

## <span data-ttu-id="c1527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1527-102">SYNOPSIS</span></span>
<span data-ttu-id="c1527-103">Получает Azure Web Apps в указанную группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1527-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="c1527-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c1527-104">SYNTAX</span></span>

### <span data-ttu-id="c1527-105">S1</span><span class="sxs-lookup"><span data-stu-id="c1527-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1527-106">S2</span><span class="sxs-lookup"><span data-stu-id="c1527-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1527-107">S3</span><span class="sxs-lookup"><span data-stu-id="c1527-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1527-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1527-108">DESCRIPTION</span></span>
<span data-ttu-id="c1527-109">С **помощью cmdlet Get-AzWebApp** можно получить сведения об Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c1527-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="c1527-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c1527-110">EXAMPLES</span></span>

### <span data-ttu-id="c1527-111">Пример 1. Получить веб-приложение из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c1527-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c1527-112">Эта команда возвращает веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c1527-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c1527-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1527-113">PARAMETERS</span></span>

### <span data-ttu-id="c1527-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c1527-114">-AppServicePlan</span></span>
<span data-ttu-id="c1527-115">Объект App Service Plan</span><span class="sxs-lookup"><span data-stu-id="c1527-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1527-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1527-116">-DefaultProfile</span></span>
<span data-ttu-id="c1527-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1527-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1527-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c1527-118">-Location</span></span>
<span data-ttu-id="c1527-119">Расположение</span><span class="sxs-lookup"><span data-stu-id="c1527-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1527-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c1527-120">-Name</span></span>
<span data-ttu-id="c1527-121">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c1527-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1527-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1527-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1527-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c1527-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1527-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1527-124">CommonParameters</span></span>
<span data-ttu-id="c1527-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1527-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1527-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1527-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1527-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1527-127">INPUTS</span></span>

### <span data-ttu-id="c1527-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c1527-128">System.String</span></span>

## <span data-ttu-id="c1527-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c1527-129">OUTPUTS</span></span>

### <span data-ttu-id="c1527-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c1527-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c1527-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c1527-131">NOTES</span></span>

## <span data-ttu-id="c1527-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1527-132">RELATED LINKS</span></span>

[<span data-ttu-id="c1527-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1527-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c1527-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1527-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c1527-135">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1527-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c1527-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1527-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c1527-137">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1527-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


