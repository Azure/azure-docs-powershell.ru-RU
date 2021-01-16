---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414852"
---
# <span data-ttu-id="7c11f-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7c11f-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="7c11f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c11f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c11f-103">Позволяет получить снимки, доступные в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="7c11f-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="7c11f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7c11f-104">SYNTAX</span></span>

### <span data-ttu-id="7c11f-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7c11f-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c11f-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7c11f-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c11f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c11f-107">DESCRIPTION</span></span>
<span data-ttu-id="7c11f-108">**Cmdlet Get-AzWebAppSnapshot** возвращает все моментальные снимки веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c11f-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="7c11f-109">Моментальные снимки — это автоматическое резервное копирование файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c11f-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="7c11f-110">Моментальный снимок можно восстановить с помощью **cmdlet Restore-AzWebAppSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="7c11f-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="7c11f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7c11f-111">EXAMPLES</span></span>

### <span data-ttu-id="7c11f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c11f-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="7c11f-113">Снимок веб-приложения ContosoApp с слотом "Промежуточное значение" в группе ресурсов Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="7c11f-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="7c11f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c11f-114">PARAMETERS</span></span>

### <span data-ttu-id="7c11f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c11f-115">-DefaultProfile</span></span>
<span data-ttu-id="7c11f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c11f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c11f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7c11f-117">-Name</span></span>
<span data-ttu-id="7c11f-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c11f-118">The name of the web app.</span></span>

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

### <span data-ttu-id="7c11f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c11f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c11f-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c11f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="7c11f-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="7c11f-121">-Slot</span></span>
<span data-ttu-id="7c11f-122">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7c11f-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="7c11f-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="7c11f-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="7c11f-124">Просмотр снимков из единицы дополнительного масштаба.</span><span class="sxs-lookup"><span data-stu-id="7c11f-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="7c11f-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7c11f-125">-WebApp</span></span>
<span data-ttu-id="7c11f-126">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7c11f-126">The web app object</span></span>

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

### <span data-ttu-id="7c11f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c11f-127">CommonParameters</span></span>
<span data-ttu-id="7c11f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c11f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c11f-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c11f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c11f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c11f-130">INPUTS</span></span>

### <span data-ttu-id="7c11f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7c11f-131">System.String</span></span>

### <span data-ttu-id="7c11f-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7c11f-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7c11f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7c11f-133">OUTPUTS</span></span>

### <span data-ttu-id="7c11f-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7c11f-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="7c11f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7c11f-135">NOTES</span></span>

## <span data-ttu-id="7c11f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c11f-136">RELATED LINKS</span></span>
