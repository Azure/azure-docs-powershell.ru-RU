---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: c6d5809211910987e06cff024d7510a70ad71a4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913255"
---
# <span data-ttu-id="24288-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="24288-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="24288-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24288-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24288-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24288-103">SYNTAX</span></span>

### <span data-ttu-id="24288-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="24288-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24288-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="24288-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24288-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24288-106">DESCRIPTION</span></span>
<span data-ttu-id="24288-107">Командлет **Get-AzureRmWebAppBackup** получает указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="24288-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="24288-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24288-108">EXAMPLES</span></span>

### <span data-ttu-id="24288-109">1:</span><span class="sxs-lookup"><span data-stu-id="24288-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="24288-110">Эта команда получает резервную копию с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="24288-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="24288-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24288-111">PARAMETERS</span></span>

### <span data-ttu-id="24288-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="24288-112">-BackupId</span></span>
<span data-ttu-id="24288-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="24288-113">Backup Id</span></span>

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

### <span data-ttu-id="24288-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24288-114">-DefaultProfile</span></span>
<span data-ttu-id="24288-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24288-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24288-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24288-116">-Name</span></span>
<span data-ttu-id="24288-117">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="24288-117">Webapp Name</span></span>

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

### <span data-ttu-id="24288-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24288-118">-ResourceGroupName</span></span>
<span data-ttu-id="24288-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="24288-119">Resource Group Name</span></span>

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

### <span data-ttu-id="24288-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="24288-120">-Slot</span></span>
<span data-ttu-id="24288-121">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="24288-121">Slot Name</span></span>

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

### <span data-ttu-id="24288-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="24288-122">-WebApp</span></span>
<span data-ttu-id="24288-123">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="24288-123">Piped WebApp</span></span>

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

### <span data-ttu-id="24288-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24288-124">CommonParameters</span></span>
<span data-ttu-id="24288-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24288-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24288-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24288-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24288-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24288-127">INPUTS</span></span>

### <span data-ttu-id="24288-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="24288-128">Site</span></span>
<span data-ttu-id="24288-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="24288-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="24288-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24288-130">OUTPUTS</span></span>

### <span data-ttu-id="24288-131">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="24288-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="24288-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="24288-132">NOTES</span></span>

## <span data-ttu-id="24288-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24288-133">RELATED LINKS</span></span>

