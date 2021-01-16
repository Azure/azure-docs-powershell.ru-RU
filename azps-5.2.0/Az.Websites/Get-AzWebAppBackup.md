---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326903"
---
# <span data-ttu-id="5f8ff-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5f8ff-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="5f8ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f8ff-102">SYNOPSIS</span></span>

## <span data-ttu-id="5f8ff-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f8ff-103">SYNTAX</span></span>

### <span data-ttu-id="5f8ff-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5f8ff-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f8ff-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5f8ff-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f8ff-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f8ff-106">DESCRIPTION</span></span>
<span data-ttu-id="5f8ff-107">Для получения указанной резервной копии Azure Web App возвращается **cmdlet Get-AzWebAppBackup.**</span><span class="sxs-lookup"><span data-stu-id="5f8ff-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="5f8ff-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f8ff-108">EXAMPLES</span></span>

### <span data-ttu-id="5f8ff-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f8ff-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="5f8ff-110">Эта команда получает резервную копию с ИД 12345 из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5f8ff-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5f8ff-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f8ff-111">PARAMETERS</span></span>

### <span data-ttu-id="5f8ff-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="5f8ff-112">-BackupId</span></span>
<span data-ttu-id="5f8ff-113">Код резервного копирования</span><span class="sxs-lookup"><span data-stu-id="5f8ff-113">Backup Id</span></span>

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

### <span data-ttu-id="5f8ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8ff-114">-DefaultProfile</span></span>
<span data-ttu-id="5f8ff-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f8ff-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5f8ff-116">-Name</span></span>
<span data-ttu-id="5f8ff-117">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="5f8ff-117">Webapp Name</span></span>

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

### <span data-ttu-id="5f8ff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8ff-118">-ResourceGroupName</span></span>
<span data-ttu-id="5f8ff-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5f8ff-119">Resource Group Name</span></span>

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

### <span data-ttu-id="5f8ff-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="5f8ff-120">-Slot</span></span>
<span data-ttu-id="5f8ff-121">Название слота</span><span class="sxs-lookup"><span data-stu-id="5f8ff-121">Slot Name</span></span>

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

### <span data-ttu-id="5f8ff-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5f8ff-122">-WebApp</span></span>
<span data-ttu-id="5f8ff-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="5f8ff-123">Piped WebApp</span></span>

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

### <span data-ttu-id="5f8ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8ff-124">CommonParameters</span></span>
<span data-ttu-id="5f8ff-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8ff-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8ff-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8ff-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f8ff-127">INPUTS</span></span>

### <span data-ttu-id="5f8ff-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f8ff-128">System.String</span></span>

### <span data-ttu-id="5f8ff-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5f8ff-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5f8ff-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f8ff-130">OUTPUTS</span></span>

### <span data-ttu-id="5f8ff-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5f8ff-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="5f8ff-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f8ff-132">NOTES</span></span>

## <span data-ttu-id="5f8ff-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f8ff-133">RELATED LINKS</span></span>