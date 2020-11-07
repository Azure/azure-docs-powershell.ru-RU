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
ms.locfileid: "93728364"
---
# <span data-ttu-id="6a901-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="6a901-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="6a901-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a901-102">SYNOPSIS</span></span>

## <span data-ttu-id="6a901-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a901-103">SYNTAX</span></span>

### <span data-ttu-id="6a901-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6a901-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a901-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6a901-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a901-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a901-106">DESCRIPTION</span></span>
<span data-ttu-id="6a901-107">Командлет **Get-AzWebAppBackupList** получает список резервных копий для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6a901-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="6a901-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a901-108">EXAMPLES</span></span>

### <span data-ttu-id="6a901-109">1:</span><span class="sxs-lookup"><span data-stu-id="6a901-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="6a901-110">Эта команда возвращает список резервных копий, относящийся к WebApp WebAppStandard, связанному с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6a901-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="6a901-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a901-111">PARAMETERS</span></span>

### <span data-ttu-id="6a901-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a901-112">-DefaultProfile</span></span>
<span data-ttu-id="6a901-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a901-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a901-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a901-114">-Name</span></span>
<span data-ttu-id="6a901-115">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6a901-115">WebApp Name</span></span>

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

### <span data-ttu-id="6a901-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a901-116">-ResourceGroupName</span></span>
<span data-ttu-id="6a901-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6a901-117">Resource Group Name</span></span>

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

### <span data-ttu-id="6a901-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="6a901-118">-Slot</span></span>
<span data-ttu-id="6a901-119">Название гнезда</span><span class="sxs-lookup"><span data-stu-id="6a901-119">Slot name</span></span>

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

### <span data-ttu-id="6a901-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6a901-120">-WebApp</span></span>
<span data-ttu-id="6a901-121">ПоWebApp повышено</span><span class="sxs-lookup"><span data-stu-id="6a901-121">Piped WebApp</span></span>

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

### <span data-ttu-id="6a901-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a901-122">CommonParameters</span></span>
<span data-ttu-id="6a901-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a901-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a901-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a901-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a901-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a901-125">INPUTS</span></span>

### <span data-ttu-id="6a901-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6a901-126">System.String</span></span>

### <span data-ttu-id="6a901-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="6a901-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6a901-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a901-128">OUTPUTS</span></span>

### <span data-ttu-id="6a901-129">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6a901-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="6a901-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a901-130">NOTES</span></span>

## <span data-ttu-id="6a901-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a901-131">RELATED LINKS</span></span>
