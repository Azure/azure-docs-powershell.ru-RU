---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505778"
---
# <span data-ttu-id="1beee-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1beee-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1beee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1beee-102">SYNOPSIS</span></span>
<span data-ttu-id="1beee-103">Позволяет получить снимки, доступные в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="1beee-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="1beee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1beee-104">SYNTAX</span></span>

### <span data-ttu-id="1beee-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1beee-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1beee-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1beee-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1beee-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1beee-107">DESCRIPTION</span></span>
<span data-ttu-id="1beee-108">**Cmdlet Get-AzWebAppSnapshot** возвращает все снимки веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1beee-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="1beee-109">Моментальные снимки — это автоматическое резервное копирование файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1beee-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="1beee-110">Моментальный снимок можно восстановить с помощью **cmdlet Restore-AzWebAppSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="1beee-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="1beee-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1beee-111">EXAMPLES</span></span>

### <span data-ttu-id="1beee-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1beee-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="1beee-113">Снимок веб-приложения ContosoApp с слотом "Промежуточное значение" в группе ресурсов Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="1beee-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="1beee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1beee-114">PARAMETERS</span></span>

### <span data-ttu-id="1beee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1beee-115">-DefaultProfile</span></span>
<span data-ttu-id="1beee-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1beee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1beee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1beee-117">-Name</span></span>
<span data-ttu-id="1beee-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1beee-118">The name of the web app.</span></span>

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

### <span data-ttu-id="1beee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1beee-119">-ResourceGroupName</span></span>
<span data-ttu-id="1beee-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1beee-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1beee-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="1beee-121">-Slot</span></span>
<span data-ttu-id="1beee-122">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1beee-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1beee-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1beee-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="1beee-124">Просмотр снимков из единицы дополнительного масштаба.</span><span class="sxs-lookup"><span data-stu-id="1beee-124">Read the snapshots from a secondary scale unit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1beee-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1beee-125">-WebApp</span></span>
<span data-ttu-id="1beee-126">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="1beee-126">The web app object</span></span>

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

### <span data-ttu-id="1beee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1beee-127">CommonParameters</span></span>
<span data-ttu-id="1beee-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1beee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1beee-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1beee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1beee-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1beee-130">INPUTS</span></span>

### <span data-ttu-id="1beee-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1beee-131">System.String</span></span>

### <span data-ttu-id="1beee-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1beee-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1beee-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1beee-133">OUTPUTS</span></span>

### <span data-ttu-id="1beee-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1beee-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1beee-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1beee-135">NOTES</span></span>

## <span data-ttu-id="1beee-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1beee-136">RELATED LINKS</span></span>
