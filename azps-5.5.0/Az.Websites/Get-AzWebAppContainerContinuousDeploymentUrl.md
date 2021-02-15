---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232273"
---
# <span data-ttu-id="926c6-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="926c6-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="926c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926c6-102">SYNOPSIS</span></span>
<span data-ttu-id="926c6-103">Get-AzWebAppContainerContinuousDeploymentUrl возвращает URL-адрес непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="926c6-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="926c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="926c6-104">SYNTAX</span></span>

### <span data-ttu-id="926c6-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="926c6-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="926c6-106">S2</span><span class="sxs-lookup"><span data-stu-id="926c6-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="926c6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="926c6-107">DESCRIPTION</span></span>
<span data-ttu-id="926c6-108">Get-AzWebAppContainerContinuousDeploymentUrl возвращает URL-адрес непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="926c6-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="926c6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="926c6-109">EXAMPLES</span></span>

### <span data-ttu-id="926c6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="926c6-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="926c6-111">Эта команда возвращает URL-адрес непрерывного развертывания контейнера.</span><span class="sxs-lookup"><span data-stu-id="926c6-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="926c6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="926c6-112">PARAMETERS</span></span>

### <span data-ttu-id="926c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926c6-113">-DefaultProfile</span></span>
<span data-ttu-id="926c6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="926c6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926c6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="926c6-115">-Name</span></span>
<span data-ttu-id="926c6-116">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="926c6-116">The name of the web app.</span></span>

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

### <span data-ttu-id="926c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="926c6-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="926c6-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="926c6-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="926c6-119">-SlotName</span></span>
<span data-ttu-id="926c6-120">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="926c6-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="926c6-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="926c6-121">-WebApp</span></span>
<span data-ttu-id="926c6-122">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="926c6-122">The web app object</span></span>

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

### <span data-ttu-id="926c6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926c6-123">CommonParameters</span></span>
<span data-ttu-id="926c6-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926c6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926c6-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926c6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926c6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="926c6-126">INPUTS</span></span>

### <span data-ttu-id="926c6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="926c6-127">System.String</span></span>

### <span data-ttu-id="926c6-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="926c6-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="926c6-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="926c6-129">OUTPUTS</span></span>

### <span data-ttu-id="926c6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="926c6-130">System.String</span></span>

## <span data-ttu-id="926c6-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="926c6-131">NOTES</span></span>

## <span data-ttu-id="926c6-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="926c6-132">RELATED LINKS</span></span>
