---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316275"
---
# <span data-ttu-id="c7809-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c7809-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="c7809-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7809-102">SYNOPSIS</span></span>

## <span data-ttu-id="c7809-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7809-103">SYNTAX</span></span>

### <span data-ttu-id="c7809-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c7809-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7809-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c7809-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7809-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7809-106">DESCRIPTION</span></span>
<span data-ttu-id="c7809-107">Командлет **Get-AzWebAppBackup** получает указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="c7809-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="c7809-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7809-108">EXAMPLES</span></span>

### <span data-ttu-id="c7809-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7809-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="c7809-110">Эта команда получает резервную копию с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c7809-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c7809-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7809-111">PARAMETERS</span></span>

### <span data-ttu-id="c7809-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="c7809-112">-BackupId</span></span>
<span data-ttu-id="c7809-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="c7809-113">Backup Id</span></span>

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

### <span data-ttu-id="c7809-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7809-114">-DefaultProfile</span></span>
<span data-ttu-id="c7809-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7809-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7809-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7809-116">-Name</span></span>
<span data-ttu-id="c7809-117">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="c7809-117">Webapp Name</span></span>

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

### <span data-ttu-id="c7809-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7809-118">-ResourceGroupName</span></span>
<span data-ttu-id="c7809-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c7809-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c7809-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="c7809-120">-Slot</span></span>
<span data-ttu-id="c7809-121">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="c7809-121">Slot Name</span></span>

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

### <span data-ttu-id="c7809-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c7809-122">-WebApp</span></span>
<span data-ttu-id="c7809-123">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="c7809-123">Piped WebApp</span></span>

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

### <span data-ttu-id="c7809-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7809-124">CommonParameters</span></span>
<span data-ttu-id="c7809-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7809-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7809-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7809-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7809-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7809-127">INPUTS</span></span>

### <span data-ttu-id="c7809-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c7809-128">System.String</span></span>

### <span data-ttu-id="c7809-129">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="c7809-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7809-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7809-130">OUTPUTS</span></span>

### <span data-ttu-id="c7809-131">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c7809-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c7809-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7809-132">NOTES</span></span>

## <span data-ttu-id="c7809-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7809-133">RELATED LINKS</span></span>
