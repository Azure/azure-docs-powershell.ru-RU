---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: fab8973c63e419cdef45fb79a0ad5182c46f2de5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907709"
---
# <span data-ttu-id="3820d-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="3820d-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="3820d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3820d-102">SYNOPSIS</span></span>

## <span data-ttu-id="3820d-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3820d-103">SYNTAX</span></span>

### <span data-ttu-id="3820d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="3820d-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3820d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="3820d-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3820d-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3820d-106">DESCRIPTION</span></span>
<span data-ttu-id="3820d-107">Командлет **Get-AzWebAppBackupList** получает список резервных копий для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3820d-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="3820d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3820d-108">EXAMPLES</span></span>

### <span data-ttu-id="3820d-109">1:</span><span class="sxs-lookup"><span data-stu-id="3820d-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="3820d-110">Эта команда возвращает список резервных копий, относящийся к WebApp WebAppStandard, связанному с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3820d-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="3820d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3820d-111">PARAMETERS</span></span>

### <span data-ttu-id="3820d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3820d-112">-DefaultProfile</span></span>
<span data-ttu-id="3820d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3820d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3820d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3820d-114">-Name</span></span>
<span data-ttu-id="3820d-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3820d-115">WebApp Name</span></span>

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

### <span data-ttu-id="3820d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3820d-116">-ResourceGroupName</span></span>
<span data-ttu-id="3820d-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3820d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="3820d-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="3820d-118">-Slot</span></span>
<span data-ttu-id="3820d-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="3820d-119">Slot name</span></span>

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

### <span data-ttu-id="3820d-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3820d-120">-WebApp</span></span>
<span data-ttu-id="3820d-121">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="3820d-121">Piped WebApp</span></span>

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

### <span data-ttu-id="3820d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3820d-122">CommonParameters</span></span>
<span data-ttu-id="3820d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3820d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3820d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3820d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3820d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3820d-125">INPUTS</span></span>

### <span data-ttu-id="3820d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3820d-126">System.String</span></span>

### <span data-ttu-id="3820d-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="3820d-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3820d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3820d-128">OUTPUTS</span></span>

### <span data-ttu-id="3820d-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="3820d-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="3820d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3820d-130">NOTES</span></span>

## <span data-ttu-id="3820d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3820d-131">RELATED LINKS</span></span>
