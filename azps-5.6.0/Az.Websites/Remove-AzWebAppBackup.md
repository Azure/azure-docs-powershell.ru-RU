---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d6bba1b517f238247291af251d9f510d18029af6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994650"
---
# <span data-ttu-id="aaff1-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="aaff1-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="aaff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaff1-102">SYNOPSIS</span></span>

## <span data-ttu-id="aaff1-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aaff1-103">SYNTAX</span></span>

### <span data-ttu-id="aaff1-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="aaff1-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaff1-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="aaff1-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaff1-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaff1-106">DESCRIPTION</span></span>
<span data-ttu-id="aaff1-107">С **помощью cmdlet Remove-AzWebAppBackup** удаляется указанная резервная копия Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="aaff1-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="aaff1-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aaff1-108">EXAMPLES</span></span>

### <span data-ttu-id="aaff1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aaff1-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="aaff1-110">Эта команда удаляет резервную копию с ИД "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="aaff1-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="aaff1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaff1-111">PARAMETERS</span></span>

### <span data-ttu-id="aaff1-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="aaff1-112">-BackupId</span></span>
<span data-ttu-id="aaff1-113">Код резервного копирования</span><span class="sxs-lookup"><span data-stu-id="aaff1-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaff1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaff1-114">-DefaultProfile</span></span>
<span data-ttu-id="aaff1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaff1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaff1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="aaff1-116">-Name</span></span>
<span data-ttu-id="aaff1-117">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="aaff1-117">WebApp Name</span></span>

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

### <span data-ttu-id="aaff1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaff1-118">-ResourceGroupName</span></span>
<span data-ttu-id="aaff1-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aaff1-119">Resource Group Name</span></span>

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

### <span data-ttu-id="aaff1-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="aaff1-120">-Slot</span></span>
<span data-ttu-id="aaff1-121">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="aaff1-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="aaff1-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="aaff1-122">-WebApp</span></span>
<span data-ttu-id="aaff1-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="aaff1-123">WebApp Object</span></span>

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

### <span data-ttu-id="aaff1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaff1-124">CommonParameters</span></span>
<span data-ttu-id="aaff1-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaff1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaff1-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaff1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaff1-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaff1-127">INPUTS</span></span>

### <span data-ttu-id="aaff1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="aaff1-128">System.String</span></span>

### <span data-ttu-id="aaff1-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="aaff1-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="aaff1-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aaff1-130">OUTPUTS</span></span>

### <span data-ttu-id="aaff1-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="aaff1-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="aaff1-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aaff1-132">NOTES</span></span>

## <span data-ttu-id="aaff1-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaff1-133">RELATED LINKS</span></span>
