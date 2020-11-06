---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569127"
---
# <span data-ttu-id="87b87-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="87b87-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="87b87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87b87-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b87-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87b87-103">SYNTAX</span></span>

### <span data-ttu-id="87b87-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="87b87-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b87-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="87b87-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87b87-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87b87-106">DESCRIPTION</span></span>
<span data-ttu-id="87b87-107">Командлет **Remove-AzureRmWebAppBackup** удаляет указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="87b87-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="87b87-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87b87-108">EXAMPLES</span></span>

### <span data-ttu-id="87b87-109">1:</span><span class="sxs-lookup"><span data-stu-id="87b87-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="87b87-110">Эта команда удаляет резервную копию с резервной копией с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="87b87-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="87b87-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87b87-111">PARAMETERS</span></span>

### <span data-ttu-id="87b87-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="87b87-112">-BackupId</span></span>
<span data-ttu-id="87b87-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="87b87-113">Backup Id</span></span>

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

### <span data-ttu-id="87b87-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87b87-114">-Name</span></span>
<span data-ttu-id="87b87-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="87b87-115">WebApp Name</span></span>

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

### <span data-ttu-id="87b87-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b87-116">-ResourceGroupName</span></span>
<span data-ttu-id="87b87-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="87b87-117">Resource Group Name</span></span>

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

### <span data-ttu-id="87b87-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="87b87-118">-Slot</span></span>
<span data-ttu-id="87b87-119">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="87b87-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="87b87-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="87b87-120">-WebApp</span></span>
<span data-ttu-id="87b87-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="87b87-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87b87-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b87-122">-DefaultProfile</span></span>
<span data-ttu-id="87b87-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87b87-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b87-124">CommonParameters</span></span>
<span data-ttu-id="87b87-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87b87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b87-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b87-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87b87-127">INPUTS</span></span>

### <span data-ttu-id="87b87-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="87b87-128">Site</span></span>
<span data-ttu-id="87b87-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="87b87-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="87b87-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87b87-130">OUTPUTS</span></span>

### <span data-ttu-id="87b87-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="87b87-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="87b87-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="87b87-132">NOTES</span></span>

## <span data-ttu-id="87b87-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87b87-133">RELATED LINKS</span></span>

