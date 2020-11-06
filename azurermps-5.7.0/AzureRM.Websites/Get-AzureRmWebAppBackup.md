---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 87ecbd0c18d90a06b986ddbe4fd00e23d28b836c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567348"
---
# <span data-ttu-id="c2dae-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c2dae-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="c2dae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2dae-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2dae-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2dae-103">SYNTAX</span></span>

### <span data-ttu-id="c2dae-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c2dae-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2dae-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c2dae-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2dae-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2dae-106">DESCRIPTION</span></span>
<span data-ttu-id="c2dae-107">Командлет **Get-AzureRmWebAppBackup** получает указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="c2dae-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="c2dae-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2dae-108">EXAMPLES</span></span>

### <span data-ttu-id="c2dae-109">1:</span><span class="sxs-lookup"><span data-stu-id="c2dae-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="c2dae-110">Эта команда получает резервную копию с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c2dae-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c2dae-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2dae-111">PARAMETERS</span></span>

### <span data-ttu-id="c2dae-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="c2dae-112">-BackupId</span></span>
<span data-ttu-id="c2dae-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="c2dae-113">Backup Id</span></span>

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

### <span data-ttu-id="c2dae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2dae-114">-DefaultProfile</span></span>
<span data-ttu-id="c2dae-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2dae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2dae-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2dae-116">-Name</span></span>
<span data-ttu-id="c2dae-117">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="c2dae-117">Webapp Name</span></span>

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

### <span data-ttu-id="c2dae-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2dae-118">-ResourceGroupName</span></span>
<span data-ttu-id="c2dae-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c2dae-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c2dae-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="c2dae-120">-Slot</span></span>
<span data-ttu-id="c2dae-121">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="c2dae-121">Slot Name</span></span>

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

### <span data-ttu-id="c2dae-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c2dae-122">-WebApp</span></span>
<span data-ttu-id="c2dae-123">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="c2dae-123">Piped WebApp</span></span>

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

### <span data-ttu-id="c2dae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2dae-124">CommonParameters</span></span>
<span data-ttu-id="c2dae-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2dae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2dae-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2dae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2dae-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2dae-127">INPUTS</span></span>

### <span data-ttu-id="c2dae-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="c2dae-128">Site</span></span>
<span data-ttu-id="c2dae-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c2dae-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c2dae-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2dae-130">OUTPUTS</span></span>

### <span data-ttu-id="c2dae-131">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c2dae-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c2dae-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2dae-132">NOTES</span></span>

## <span data-ttu-id="c2dae-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2dae-133">RELATED LINKS</span></span>

