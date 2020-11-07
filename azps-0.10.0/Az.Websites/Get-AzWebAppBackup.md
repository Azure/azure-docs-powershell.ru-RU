---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: b533d63e83d731dd5b95788609d32fa4cf7863f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910624"
---
# <span data-ttu-id="f0333-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f0333-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="f0333-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0333-102">SYNOPSIS</span></span>

## <span data-ttu-id="f0333-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0333-103">SYNTAX</span></span>

### <span data-ttu-id="f0333-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f0333-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0333-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f0333-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0333-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0333-106">DESCRIPTION</span></span>
<span data-ttu-id="f0333-107">Командлет **Get-AzWebAppBackup** получает указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f0333-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="f0333-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0333-108">EXAMPLES</span></span>

### <span data-ttu-id="f0333-109">1:</span><span class="sxs-lookup"><span data-stu-id="f0333-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="f0333-110">Эта команда получает резервную копию с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f0333-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f0333-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0333-111">PARAMETERS</span></span>

### <span data-ttu-id="f0333-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f0333-112">-BackupId</span></span>
<span data-ttu-id="f0333-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="f0333-113">Backup Id</span></span>

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

### <span data-ttu-id="f0333-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0333-114">-DefaultProfile</span></span>
<span data-ttu-id="f0333-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0333-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0333-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0333-116">-Name</span></span>
<span data-ttu-id="f0333-117">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="f0333-117">Webapp Name</span></span>

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

### <span data-ttu-id="f0333-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0333-118">-ResourceGroupName</span></span>
<span data-ttu-id="f0333-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0333-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f0333-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="f0333-120">-Slot</span></span>
<span data-ttu-id="f0333-121">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="f0333-121">Slot Name</span></span>

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

### <span data-ttu-id="f0333-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f0333-122">-WebApp</span></span>
<span data-ttu-id="f0333-123">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="f0333-123">Piped WebApp</span></span>

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

### <span data-ttu-id="f0333-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0333-124">CommonParameters</span></span>
<span data-ttu-id="f0333-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0333-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0333-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0333-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0333-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0333-127">INPUTS</span></span>

### <span data-ttu-id="f0333-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="f0333-128">Site</span></span>
<span data-ttu-id="f0333-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f0333-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f0333-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0333-130">OUTPUTS</span></span>

### <span data-ttu-id="f0333-131">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f0333-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="f0333-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0333-132">NOTES</span></span>

## <span data-ttu-id="f0333-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0333-133">RELATED LINKS</span></span>

