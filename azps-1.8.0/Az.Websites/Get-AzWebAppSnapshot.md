---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: fab46f997492c366857c7d13bea38543cca4e91c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728343"
---
# <span data-ttu-id="0020b-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0020b-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="0020b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0020b-102">SYNOPSIS</span></span>
<span data-ttu-id="0020b-103">Получает снимки, доступные для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0020b-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="0020b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0020b-104">SYNTAX</span></span>

### <span data-ttu-id="0020b-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0020b-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0020b-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0020b-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0020b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0020b-107">DESCRIPTION</span></span>
<span data-ttu-id="0020b-108">Командлет **Get-AzWebAppSnapshot** возвращает все снимки для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0020b-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="0020b-109">Моментальные снимки — это автоматические резервные копии файлов и параметров веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0020b-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="0020b-110">Снимок можно восстановить с помощью командлета **RESTORE-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="0020b-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="0020b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0020b-111">EXAMPLES</span></span>

### <span data-ttu-id="0020b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0020b-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="0020b-113">Получение моментальных снимков для веб-приложения с именем "ConstosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS"</span><span class="sxs-lookup"><span data-stu-id="0020b-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="0020b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0020b-114">PARAMETERS</span></span>

### <span data-ttu-id="0020b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0020b-115">-DefaultProfile</span></span>
<span data-ttu-id="0020b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0020b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0020b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0020b-117">-Name</span></span>
<span data-ttu-id="0020b-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0020b-118">The name of the web app.</span></span>

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

### <span data-ttu-id="0020b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0020b-119">-ResourceGroupName</span></span>
<span data-ttu-id="0020b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0020b-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0020b-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="0020b-121">-Slot</span></span>
<span data-ttu-id="0020b-122">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="0020b-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="0020b-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0020b-123">-WebApp</span></span>
<span data-ttu-id="0020b-124">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="0020b-124">The web app object</span></span>

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

### <span data-ttu-id="0020b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0020b-125">CommonParameters</span></span>
<span data-ttu-id="0020b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0020b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0020b-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0020b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0020b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0020b-128">INPUTS</span></span>

### <span data-ttu-id="0020b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0020b-129">System.String</span></span>

### <span data-ttu-id="0020b-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="0020b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0020b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0020b-131">OUTPUTS</span></span>

### <span data-ttu-id="0020b-132">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0020b-132">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="0020b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0020b-133">NOTES</span></span>

## <span data-ttu-id="0020b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0020b-134">RELATED LINKS</span></span>
