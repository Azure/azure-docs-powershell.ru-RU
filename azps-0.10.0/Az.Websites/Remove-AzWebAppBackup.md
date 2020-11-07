---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d8c25931e5eeae035f319c36698369b865500b9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910587"
---
# <span data-ttu-id="659ac-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="659ac-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="659ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="659ac-102">SYNOPSIS</span></span>

## <span data-ttu-id="659ac-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="659ac-103">SYNTAX</span></span>

### <span data-ttu-id="659ac-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="659ac-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="659ac-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="659ac-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="659ac-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="659ac-106">DESCRIPTION</span></span>
<span data-ttu-id="659ac-107">Командлет **Remove-AzWebAppBackup** удаляет указанную резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="659ac-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="659ac-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="659ac-108">EXAMPLES</span></span>

### <span data-ttu-id="659ac-109">1:</span><span class="sxs-lookup"><span data-stu-id="659ac-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="659ac-110">Эта команда удаляет резервную копию с резервной копией с ИДЕНТИФИКАТОРом "12345" из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="659ac-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="659ac-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="659ac-111">PARAMETERS</span></span>

### <span data-ttu-id="659ac-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="659ac-112">-BackupId</span></span>
<span data-ttu-id="659ac-113">Идентификатор резервного копирования</span><span class="sxs-lookup"><span data-stu-id="659ac-113">Backup Id</span></span>

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

### <span data-ttu-id="659ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659ac-114">-DefaultProfile</span></span>
<span data-ttu-id="659ac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="659ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="659ac-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="659ac-116">-Name</span></span>
<span data-ttu-id="659ac-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="659ac-117">WebApp Name</span></span>

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

### <span data-ttu-id="659ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="659ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="659ac-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="659ac-119">Resource Group Name</span></span>

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

### <span data-ttu-id="659ac-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="659ac-120">-Slot</span></span>
<span data-ttu-id="659ac-121">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="659ac-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="659ac-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="659ac-122">-WebApp</span></span>
<span data-ttu-id="659ac-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="659ac-123">WebApp Object</span></span>

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

### <span data-ttu-id="659ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659ac-124">CommonParameters</span></span>
<span data-ttu-id="659ac-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="659ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659ac-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="659ac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659ac-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="659ac-127">INPUTS</span></span>

### <span data-ttu-id="659ac-128">Семейств</span><span class="sxs-lookup"><span data-stu-id="659ac-128">Site</span></span>
<span data-ttu-id="659ac-129">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="659ac-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="659ac-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="659ac-130">OUTPUTS</span></span>

### <span data-ttu-id="659ac-131">Microsoft. Azure. Management. website. Models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="659ac-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="659ac-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="659ac-132">NOTES</span></span>

## <span data-ttu-id="659ac-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="659ac-133">RELATED LINKS</span></span>

