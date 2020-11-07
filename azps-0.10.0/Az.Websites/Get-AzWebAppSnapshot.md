---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910611"
---
# <span data-ttu-id="d07ad-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d07ad-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="d07ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d07ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d07ad-103">Получает снимки, доступные для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d07ad-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="d07ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d07ad-104">SYNTAX</span></span>

### <span data-ttu-id="d07ad-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d07ad-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="d07ad-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d07ad-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="d07ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d07ad-107">DESCRIPTION</span></span>
<span data-ttu-id="d07ad-108">Командлет **Get-AzWebAppSnapshot** возвращает все снимки для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d07ad-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="d07ad-109">Моментальные снимки — это автоматические резервные копии файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d07ad-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="d07ad-110">Снимок можно восстановить с помощью командлета **RESTORE-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="d07ad-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="d07ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d07ad-111">EXAMPLES</span></span>

### <span data-ttu-id="d07ad-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d07ad-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="d07ad-113">Получение моментальных снимков для веб-приложения с именем "ConstosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="d07ad-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="d07ad-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d07ad-114">PARAMETERS</span></span>

### <span data-ttu-id="d07ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07ad-115">-DefaultProfile</span></span>
<span data-ttu-id="d07ad-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d07ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07ad-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d07ad-117">-Name</span></span>
<span data-ttu-id="d07ad-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d07ad-118">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="d07ad-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d07ad-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07ad-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="d07ad-121">-Slot</span></span>
<span data-ttu-id="d07ad-122">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d07ad-122">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d07ad-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d07ad-123">-WebApp</span></span>
<span data-ttu-id="d07ad-124">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="d07ad-124">The web app object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## <span data-ttu-id="d07ad-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d07ad-125">INPUTS</span></span>

### <span data-ttu-id="d07ad-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d07ad-126">System.String</span></span>
<span data-ttu-id="d07ad-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="d07ad-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="d07ad-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d07ad-128">OUTPUTS</span></span>

### <span data-ttu-id="d07ad-129">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d07ad-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="d07ad-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d07ad-130">NOTES</span></span>

## <span data-ttu-id="d07ad-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d07ad-131">RELATED LINKS</span></span>

