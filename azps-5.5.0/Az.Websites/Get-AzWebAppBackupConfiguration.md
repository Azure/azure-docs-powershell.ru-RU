---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242949"
---
# <span data-ttu-id="d2c9b-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c9b-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d2c9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c9b-102">SYNOPSIS</span></span>

## <span data-ttu-id="d2c9b-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2c9b-103">SYNTAX</span></span>

### <span data-ttu-id="d2c9b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d2c9b-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2c9b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d2c9b-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c9b-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2c9b-106">DESCRIPTION</span></span>
<span data-ttu-id="d2c9b-107">С **помощью cmdlet get-AzWebAppBackupConfiguration** можно получить резервную копию Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="d2c9b-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="d2c9b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2c9b-108">EXAMPLES</span></span>

### <span data-ttu-id="d2c9b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2c9b-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d2c9b-110">Эта команда получает конфигурацию резервного копирования из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d2c9b-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d2c9b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c9b-111">PARAMETERS</span></span>

### <span data-ttu-id="d2c9b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c9b-112">-DefaultProfile</span></span>
<span data-ttu-id="d2c9b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2c9b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c9b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d2c9b-114">-Name</span></span>
<span data-ttu-id="d2c9b-115">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="d2c9b-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c9b-116">-ResourceGroupName</span></span>
<span data-ttu-id="d2c9b-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d2c9b-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9b-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="d2c9b-118">-Slot</span></span>
<span data-ttu-id="d2c9b-119">Название слота</span><span class="sxs-lookup"><span data-stu-id="d2c9b-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9b-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d2c9b-120">-WebApp</span></span>
<span data-ttu-id="d2c9b-121">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="d2c9b-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c9b-122">CommonParameters</span></span>
<span data-ttu-id="d2c9b-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c9b-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c9b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c9b-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c9b-125">INPUTS</span></span>

### <span data-ttu-id="d2c9b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d2c9b-126">System.String</span></span>

### <span data-ttu-id="d2c9b-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d2c9b-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d2c9b-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c9b-128">OUTPUTS</span></span>

### <span data-ttu-id="d2c9b-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c9b-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d2c9b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2c9b-130">NOTES</span></span>

## <span data-ttu-id="d2c9b-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2c9b-131">RELATED LINKS</span></span>
