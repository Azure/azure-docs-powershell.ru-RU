---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326091"
---
# <span data-ttu-id="200f6-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="200f6-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="200f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="200f6-102">SYNOPSIS</span></span>

## <span data-ttu-id="200f6-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="200f6-103">SYNTAX</span></span>

### <span data-ttu-id="200f6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="200f6-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="200f6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="200f6-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="200f6-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="200f6-106">DESCRIPTION</span></span>
<span data-ttu-id="200f6-107">С **помощью cmdlet Remove-AzWebAppBackup** удаляется указанная резервная копия Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="200f6-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="200f6-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="200f6-108">EXAMPLES</span></span>

### <span data-ttu-id="200f6-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="200f6-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="200f6-110">Эта команда удаляет резервную копию с ИД "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="200f6-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="200f6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="200f6-111">PARAMETERS</span></span>

### <span data-ttu-id="200f6-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="200f6-112">-BackupId</span></span>
<span data-ttu-id="200f6-113">Код резервного копирования</span><span class="sxs-lookup"><span data-stu-id="200f6-113">Backup Id</span></span>

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

### <span data-ttu-id="200f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="200f6-114">-DefaultProfile</span></span>
<span data-ttu-id="200f6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="200f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="200f6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="200f6-116">-Name</span></span>
<span data-ttu-id="200f6-117">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="200f6-117">WebApp Name</span></span>

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

### <span data-ttu-id="200f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="200f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="200f6-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="200f6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="200f6-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="200f6-120">-Slot</span></span>
<span data-ttu-id="200f6-121">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="200f6-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="200f6-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="200f6-122">-WebApp</span></span>
<span data-ttu-id="200f6-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="200f6-123">WebApp Object</span></span>

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

### <span data-ttu-id="200f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="200f6-124">CommonParameters</span></span>
<span data-ttu-id="200f6-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="200f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="200f6-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="200f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="200f6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="200f6-127">INPUTS</span></span>

### <span data-ttu-id="200f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="200f6-128">System.String</span></span>

### <span data-ttu-id="200f6-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="200f6-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="200f6-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="200f6-130">OUTPUTS</span></span>

### <span data-ttu-id="200f6-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="200f6-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="200f6-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="200f6-132">NOTES</span></span>

## <span data-ttu-id="200f6-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="200f6-133">RELATED LINKS</span></span>