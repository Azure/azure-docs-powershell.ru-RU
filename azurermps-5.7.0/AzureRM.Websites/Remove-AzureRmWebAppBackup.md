---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: f2b6e4b4ea09605a55e179e682065de70ef92024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561367"
---
# <span data-ttu-id="d5d7e-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d5d7e-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="d5d7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5d7e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5d7e-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5d7e-103">SYNTAX</span></span>

### <span data-ttu-id="d5d7e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d5d7e-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d7e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d5d7e-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5d7e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d7e-106">DESCRIPTION</span></span>
<span data-ttu-id="d5d7e-107">Командлет **Remove-AzureRmWebAppBackup** удаляет указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="d5d7e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5d7e-108">EXAMPLES</span></span>

### <span data-ttu-id="d5d7e-109">1:</span><span class="sxs-lookup"><span data-stu-id="d5d7e-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="d5d7e-110">Эта команда удаляет резервную копию с резервной копией с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d5d7e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5d7e-111">PARAMETERS</span></span>

### <span data-ttu-id="d5d7e-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="d5d7e-112">-BackupId</span></span>
<span data-ttu-id="d5d7e-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="d5d7e-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5d7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d7e-114">-DefaultProfile</span></span>
<span data-ttu-id="d5d7e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5d7e-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5d7e-116">-Name</span></span>
<span data-ttu-id="d5d7e-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d5d7e-117">WebApp Name</span></span>

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

### <span data-ttu-id="d5d7e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d7e-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5d7e-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d5d7e-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d5d7e-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="d5d7e-120">-Slot</span></span>
<span data-ttu-id="d5d7e-121">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="d5d7e-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d5d7e-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d5d7e-122">-WebApp</span></span>
<span data-ttu-id="d5d7e-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="d5d7e-123">WebApp Object</span></span>

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

### <span data-ttu-id="d5d7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d7e-124">CommonParameters</span></span>
<span data-ttu-id="d5d7e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d7e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d7e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5d7e-127">INPUTS</span></span>

### <span data-ttu-id="d5d7e-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="d5d7e-128">Site</span></span>
<span data-ttu-id="d5d7e-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5d7e-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d5d7e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d7e-130">OUTPUTS</span></span>

### <span data-ttu-id="d5d7e-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="d5d7e-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="d5d7e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5d7e-132">NOTES</span></span>

## <span data-ttu-id="d5d7e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5d7e-133">RELATED LINKS</span></span>

