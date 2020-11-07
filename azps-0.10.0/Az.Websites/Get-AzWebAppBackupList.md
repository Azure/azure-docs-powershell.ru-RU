---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 057bebde5eada143c9ee00260a1406fdceae9436
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910622"
---
# <span data-ttu-id="71d3d-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="71d3d-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="71d3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71d3d-102">SYNOPSIS</span></span>

## <span data-ttu-id="71d3d-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71d3d-103">SYNTAX</span></span>

### <span data-ttu-id="71d3d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="71d3d-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71d3d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="71d3d-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d3d-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d3d-106">DESCRIPTION</span></span>
<span data-ttu-id="71d3d-107">Командлет **Get-AzWebAppBackupList** получает список резервных копий для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="71d3d-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="71d3d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71d3d-108">EXAMPLES</span></span>

### <span data-ttu-id="71d3d-109">1:</span><span class="sxs-lookup"><span data-stu-id="71d3d-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="71d3d-110">Эта команда возвращает список резервных копий, относящийся к WebApp WebAppStandard, связанному с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71d3d-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="71d3d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71d3d-111">PARAMETERS</span></span>

### <span data-ttu-id="71d3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d3d-112">-DefaultProfile</span></span>
<span data-ttu-id="71d3d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71d3d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71d3d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71d3d-114">-Name</span></span>
<span data-ttu-id="71d3d-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="71d3d-115">WebApp Name</span></span>

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

### <span data-ttu-id="71d3d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71d3d-116">-ResourceGroupName</span></span>
<span data-ttu-id="71d3d-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="71d3d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="71d3d-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="71d3d-118">-Slot</span></span>
<span data-ttu-id="71d3d-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="71d3d-119">Slot name</span></span>

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

### <span data-ttu-id="71d3d-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71d3d-120">-WebApp</span></span>
<span data-ttu-id="71d3d-121">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="71d3d-121">Piped WebApp</span></span>

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

### <span data-ttu-id="71d3d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d3d-122">CommonParameters</span></span>
<span data-ttu-id="71d3d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71d3d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d3d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d3d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d3d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71d3d-125">INPUTS</span></span>

### <span data-ttu-id="71d3d-126">Семейств</span><span class="sxs-lookup"><span data-stu-id="71d3d-126">Site</span></span>
<span data-ttu-id="71d3d-127">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="71d3d-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="71d3d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71d3d-128">OUTPUTS</span></span>

### <span data-ttu-id="71d3d-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="71d3d-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="71d3d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="71d3d-130">NOTES</span></span>

## <span data-ttu-id="71d3d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71d3d-131">RELATED LINKS</span></span>

