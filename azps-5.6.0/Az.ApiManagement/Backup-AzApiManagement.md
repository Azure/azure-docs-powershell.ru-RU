---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 1f0ceb4f349e7fdfee38837561dc436c16cd451b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991780"
---
# <span data-ttu-id="3b145-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b145-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="3b145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b145-102">SYNOPSIS</span></span>
<span data-ttu-id="3b145-103">Backs up an API Management service.</span><span class="sxs-lookup"><span data-stu-id="3b145-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="3b145-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b145-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b145-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b145-105">DESCRIPTION</span></span>
<span data-ttu-id="3b145-106">Для **выполнения командылет Backup-AzApiManagement** резервная копия экземпляра службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="3b145-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="3b145-107">Этот cmdlet хранит резервную копию как BLOB-проект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3b145-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="3b145-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b145-108">EXAMPLES</span></span>

### <span data-ttu-id="3b145-109">Пример 1. Back up an API Management service (Управление API)</span><span class="sxs-lookup"><span data-stu-id="3b145-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="3b145-110">Эта команда возвращает службу управления API в большой бизнес-бизнес хранилища.</span><span class="sxs-lookup"><span data-stu-id="3b145-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="3b145-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b145-111">PARAMETERS</span></span>

### <span data-ttu-id="3b145-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b145-112">-DefaultProfile</span></span>
<span data-ttu-id="3b145-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b145-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b145-114">-Name</span><span class="sxs-lookup"><span data-stu-id="3b145-114">-Name</span></span>
<span data-ttu-id="3b145-115">Указывает имя развертывания управления API, которое этот cmdlet backs up.</span><span class="sxs-lookup"><span data-stu-id="3b145-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b145-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b145-116">-PassThru</span></span>
<span data-ttu-id="3b145-117">Указывает на то, что этот cmdlet возвращает объект **PsApiManagement,** который был возвращен в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="3b145-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b145-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b145-118">-ResourceGroupName</span></span>
<span data-ttu-id="3b145-119">Имя группы ресурсов, в которой развернуто управление API.</span><span class="sxs-lookup"><span data-stu-id="3b145-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b145-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="3b145-120">-StorageContext</span></span>
<span data-ttu-id="3b145-121">Определяет контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3b145-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b145-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="3b145-122">-TargetBlobName</span></span>
<span data-ttu-id="3b145-123">Имя BLOB-части для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b145-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="3b145-124">Если BLOB-проект не существует, он создается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b145-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="3b145-125">Этот cmdlet создает значение по умолчанию на основе следующего шаблона: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="3b145-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b145-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="3b145-126">-TargetContainerName</span></span>
<span data-ttu-id="3b145-127">Имя контейнера BLOB-части для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b145-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="3b145-128">Если контейнера нет, он создается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b145-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b145-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b145-129">CommonParameters</span></span>
<span data-ttu-id="3b145-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b145-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b145-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b145-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b145-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b145-132">INPUTS</span></span>

### <span data-ttu-id="3b145-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3b145-133">System.String</span></span>

### <span data-ttu-id="3b145-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b145-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b145-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b145-135">OUTPUTS</span></span>

### <span data-ttu-id="3b145-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b145-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3b145-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b145-137">NOTES</span></span>

## <span data-ttu-id="3b145-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b145-138">RELATED LINKS</span></span>

[<span data-ttu-id="3b145-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b145-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="3b145-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b145-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="3b145-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b145-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="3b145-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3b145-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


