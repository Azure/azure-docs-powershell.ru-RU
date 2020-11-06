---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupList.md
ms.openlocfilehash: f4005df31746b63b2a45fa2c78f254e2d5f24c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558120"
---
# <span data-ttu-id="21a81-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="21a81-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="21a81-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21a81-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a81-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21a81-103">SYNTAX</span></span>

### <span data-ttu-id="21a81-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="21a81-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21a81-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="21a81-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21a81-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21a81-106">DESCRIPTION</span></span>
<span data-ttu-id="21a81-107">Командлет **Get-AzureRmWebAppBackupList** получает список резервных копий для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="21a81-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="21a81-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21a81-108">EXAMPLES</span></span>

### <span data-ttu-id="21a81-109">1:</span><span class="sxs-lookup"><span data-stu-id="21a81-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="21a81-110">Эта команда возвращает список резервных копий, относящийся к WebApp WebAppStandard, связанному с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="21a81-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="21a81-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21a81-111">PARAMETERS</span></span>

### <span data-ttu-id="21a81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a81-112">-DefaultProfile</span></span>
<span data-ttu-id="21a81-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21a81-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a81-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21a81-114">-Name</span></span>
<span data-ttu-id="21a81-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="21a81-115">WebApp Name</span></span>

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

### <span data-ttu-id="21a81-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a81-116">-ResourceGroupName</span></span>
<span data-ttu-id="21a81-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="21a81-117">Resource Group Name</span></span>

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

### <span data-ttu-id="21a81-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="21a81-118">-Slot</span></span>
<span data-ttu-id="21a81-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="21a81-119">Slot name</span></span>

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

### <span data-ttu-id="21a81-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="21a81-120">-WebApp</span></span>
<span data-ttu-id="21a81-121">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="21a81-121">Piped WebApp</span></span>

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

### <span data-ttu-id="21a81-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a81-122">CommonParameters</span></span>
<span data-ttu-id="21a81-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21a81-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a81-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21a81-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a81-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21a81-125">INPUTS</span></span>

### <span data-ttu-id="21a81-126">System. String</span><span class="sxs-lookup"><span data-stu-id="21a81-126">System.String</span></span>

### <span data-ttu-id="21a81-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="21a81-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="21a81-128">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="21a81-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="21a81-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21a81-129">OUTPUTS</span></span>

### <span data-ttu-id="21a81-130">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="21a81-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="21a81-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="21a81-131">NOTES</span></span>

## <span data-ttu-id="21a81-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21a81-132">RELATED LINKS</span></span>
