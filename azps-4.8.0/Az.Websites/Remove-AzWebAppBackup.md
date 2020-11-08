---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079310"
---
# <span data-ttu-id="6154f-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6154f-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="6154f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6154f-102">SYNOPSIS</span></span>

## <span data-ttu-id="6154f-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6154f-103">SYNTAX</span></span>

### <span data-ttu-id="6154f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6154f-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6154f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6154f-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6154f-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6154f-106">DESCRIPTION</span></span>
<span data-ttu-id="6154f-107">Командлет **Remove-AzWebAppBackup** удаляет указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6154f-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="6154f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6154f-108">EXAMPLES</span></span>

### <span data-ttu-id="6154f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6154f-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="6154f-110">Эта команда удаляет резервную копию с резервной копией с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6154f-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6154f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6154f-111">PARAMETERS</span></span>

### <span data-ttu-id="6154f-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="6154f-112">-BackupId</span></span>
<span data-ttu-id="6154f-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="6154f-113">Backup Id</span></span>

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

### <span data-ttu-id="6154f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6154f-114">-DefaultProfile</span></span>
<span data-ttu-id="6154f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6154f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6154f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6154f-116">-Name</span></span>
<span data-ttu-id="6154f-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6154f-117">WebApp Name</span></span>

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

### <span data-ttu-id="6154f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6154f-118">-ResourceGroupName</span></span>
<span data-ttu-id="6154f-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6154f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="6154f-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="6154f-120">-Slot</span></span>
<span data-ttu-id="6154f-121">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="6154f-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6154f-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6154f-122">-WebApp</span></span>
<span data-ttu-id="6154f-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6154f-123">WebApp Object</span></span>

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

### <span data-ttu-id="6154f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6154f-124">CommonParameters</span></span>
<span data-ttu-id="6154f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6154f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6154f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6154f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6154f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6154f-127">INPUTS</span></span>

### <span data-ttu-id="6154f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6154f-128">System.String</span></span>

### <span data-ttu-id="6154f-129">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="6154f-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6154f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6154f-130">OUTPUTS</span></span>

### <span data-ttu-id="6154f-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="6154f-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="6154f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="6154f-132">NOTES</span></span>

## <span data-ttu-id="6154f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6154f-133">RELATED LINKS</span></span>
