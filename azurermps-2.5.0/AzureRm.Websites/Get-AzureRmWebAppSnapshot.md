---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913413"
---
# <span data-ttu-id="8cb37-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8cb37-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="8cb37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cb37-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb37-103">Получает снимки, доступные для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8cb37-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cb37-104">SYNTAX</span></span>

### <span data-ttu-id="8cb37-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8cb37-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="8cb37-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8cb37-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="8cb37-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cb37-107">DESCRIPTION</span></span>
<span data-ttu-id="8cb37-108">Командлет **Get-AzureRmWebAppSnapshot** возвращает все снимки для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8cb37-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="8cb37-109">Моментальные снимки — это автоматические резервные копии файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8cb37-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="8cb37-110">Снимок можно восстановить с помощью командлета **RESTORE-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="8cb37-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="8cb37-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cb37-111">EXAMPLES</span></span>

### <span data-ttu-id="8cb37-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8cb37-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="8cb37-113">Получение моментальных снимков для веб-приложения с именем "ConstosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="8cb37-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="8cb37-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cb37-114">PARAMETERS</span></span>

### <span data-ttu-id="8cb37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb37-115">-DefaultProfile</span></span>
<span data-ttu-id="8cb37-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cb37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb37-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cb37-117">-Name</span></span>
<span data-ttu-id="8cb37-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8cb37-118">The name of the web app.</span></span>

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

### <span data-ttu-id="8cb37-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb37-119">-ResourceGroupName</span></span>
<span data-ttu-id="8cb37-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8cb37-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="8cb37-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="8cb37-121">-Slot</span></span>
<span data-ttu-id="8cb37-122">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="8cb37-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="8cb37-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8cb37-123">-WebApp</span></span>
<span data-ttu-id="8cb37-124">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="8cb37-124">The web app object</span></span>

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

## <span data-ttu-id="8cb37-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cb37-125">INPUTS</span></span>

### <span data-ttu-id="8cb37-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8cb37-126">System.String</span></span>
<span data-ttu-id="8cb37-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="8cb37-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="8cb37-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cb37-128">OUTPUTS</span></span>

### <span data-ttu-id="8cb37-129">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="8cb37-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="8cb37-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cb37-130">NOTES</span></span>

## <span data-ttu-id="8cb37-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cb37-131">RELATED LINKS</span></span>

