---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243434"
---
# <span data-ttu-id="1616d-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1616d-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1616d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1616d-102">SYNOPSIS</span></span>
<span data-ttu-id="1616d-103">Получает снимки, доступные для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1616d-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="1616d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1616d-104">SYNTAX</span></span>

### <span data-ttu-id="1616d-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1616d-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1616d-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1616d-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1616d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1616d-107">DESCRIPTION</span></span>
<span data-ttu-id="1616d-108">Командлет **Get-AzWebAppSnapshot** возвращает все снимки для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1616d-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="1616d-109">Моментальные снимки — это автоматические резервные копии файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1616d-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="1616d-110">Снимок можно восстановить с помощью командлета **RESTORE-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="1616d-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="1616d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1616d-111">EXAMPLES</span></span>

### <span data-ttu-id="1616d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1616d-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="1616d-113">Получение моментальных снимков для веб-приложения с именем "ContosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="1616d-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="1616d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1616d-114">PARAMETERS</span></span>

### <span data-ttu-id="1616d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1616d-115">-DefaultProfile</span></span>
<span data-ttu-id="1616d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1616d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1616d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1616d-117">-Name</span></span>
<span data-ttu-id="1616d-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1616d-118">The name of the web app.</span></span>

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

### <span data-ttu-id="1616d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1616d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1616d-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1616d-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1616d-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="1616d-121">-Slot</span></span>
<span data-ttu-id="1616d-122">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="1616d-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1616d-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1616d-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="1616d-124">Чтение снимков из дополнительного шкалы.</span><span class="sxs-lookup"><span data-stu-id="1616d-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="1616d-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1616d-125">-WebApp</span></span>
<span data-ttu-id="1616d-126">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="1616d-126">The web app object</span></span>

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

### <span data-ttu-id="1616d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1616d-127">CommonParameters</span></span>
<span data-ttu-id="1616d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1616d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1616d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1616d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1616d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1616d-130">INPUTS</span></span>

### <span data-ttu-id="1616d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1616d-131">System.String</span></span>

### <span data-ttu-id="1616d-132">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="1616d-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1616d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1616d-133">OUTPUTS</span></span>

### <span data-ttu-id="1616d-134">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1616d-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1616d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1616d-135">NOTES</span></span>

## <span data-ttu-id="1616d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1616d-136">RELATED LINKS</span></span>
