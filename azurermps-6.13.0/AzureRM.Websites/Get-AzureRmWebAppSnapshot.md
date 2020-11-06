---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556439"
---
# <span data-ttu-id="b7ff3-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b7ff3-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="b7ff3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ff3-103">Получает снимки, доступные для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7ff3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7ff3-104">SYNTAX</span></span>

### <span data-ttu-id="b7ff3-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b7ff3-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ff3-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b7ff3-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ff3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ff3-107">DESCRIPTION</span></span>
<span data-ttu-id="b7ff3-108">Командлет **Get-AzureRmWebAppSnapshot** возвращает все снимки для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="b7ff3-109">Моментальные снимки — это автоматические резервные копии файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="b7ff3-110">Снимок можно восстановить с помощью командлета **RESTORE-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="b7ff3-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="b7ff3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7ff3-111">EXAMPLES</span></span>

### <span data-ttu-id="b7ff3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7ff3-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="b7ff3-113">Получение моментальных снимков для веб-приложения с именем "ConstosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="b7ff3-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="b7ff3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7ff3-114">PARAMETERS</span></span>

### <span data-ttu-id="b7ff3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ff3-115">-DefaultProfile</span></span>
<span data-ttu-id="b7ff3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ff3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7ff3-117">-Name</span></span>
<span data-ttu-id="b7ff3-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b7ff3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ff3-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7ff3-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7ff3-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="b7ff3-121">-Slot</span></span>
<span data-ttu-id="b7ff3-122">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b7ff3-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b7ff3-123">-WebApp</span></span>
<span data-ttu-id="b7ff3-124">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b7ff3-124">The web app object</span></span>

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

### <span data-ttu-id="b7ff3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ff3-125">CommonParameters</span></span>
<span data-ttu-id="b7ff3-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ff3-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ff3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ff3-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7ff3-128">INPUTS</span></span>

### <span data-ttu-id="b7ff3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ff3-129">System.String</span></span>

### <span data-ttu-id="b7ff3-130">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="b7ff3-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b7ff3-131">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7ff3-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="b7ff3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7ff3-132">OUTPUTS</span></span>

### <span data-ttu-id="b7ff3-133">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b7ff3-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="b7ff3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7ff3-134">NOTES</span></span>

## <span data-ttu-id="b7ff3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7ff3-135">RELATED LINKS</span></span>
