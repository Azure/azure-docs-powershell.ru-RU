---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: ad27e4f9f7e042fa5a649fb06131167f38f1a1be
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914674"
---
# <span data-ttu-id="ae864-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ae864-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="ae864-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae864-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae864-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae864-103">SYNTAX</span></span>

### <span data-ttu-id="ae864-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ae864-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae864-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ae864-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae864-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae864-106">DESCRIPTION</span></span>
<span data-ttu-id="ae864-107">Командлет **Remove-AzureRmWebAppBackup** удаляет указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="ae864-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="ae864-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae864-108">EXAMPLES</span></span>

### <span data-ttu-id="ae864-109">1:</span><span class="sxs-lookup"><span data-stu-id="ae864-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="ae864-110">Эта команда удаляет резервную копию с резервной копией с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ae864-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ae864-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae864-111">PARAMETERS</span></span>

### <span data-ttu-id="ae864-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="ae864-112">-BackupId</span></span>
<span data-ttu-id="ae864-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="ae864-113">Backup Id</span></span>

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

### <span data-ttu-id="ae864-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae864-114">-DefaultProfile</span></span>
<span data-ttu-id="ae864-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae864-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae864-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae864-116">-Name</span></span>
<span data-ttu-id="ae864-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ae864-117">WebApp Name</span></span>

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

### <span data-ttu-id="ae864-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae864-118">-ResourceGroupName</span></span>
<span data-ttu-id="ae864-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ae864-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ae864-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="ae864-120">-Slot</span></span>
<span data-ttu-id="ae864-121">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="ae864-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ae864-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ae864-122">-WebApp</span></span>
<span data-ttu-id="ae864-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ae864-123">WebApp Object</span></span>

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

### <span data-ttu-id="ae864-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae864-124">CommonParameters</span></span>
<span data-ttu-id="ae864-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae864-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae864-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae864-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae864-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae864-127">INPUTS</span></span>

### <span data-ttu-id="ae864-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="ae864-128">Site</span></span>
<span data-ttu-id="ae864-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ae864-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ae864-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae864-130">OUTPUTS</span></span>

### <span data-ttu-id="ae864-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="ae864-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="ae864-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae864-132">NOTES</span></span>

## <span data-ttu-id="ae864-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae864-133">RELATED LINKS</span></span>

