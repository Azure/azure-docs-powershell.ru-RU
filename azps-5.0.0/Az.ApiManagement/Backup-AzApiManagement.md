---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315449"
---
# <span data-ttu-id="5d576-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d576-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="5d576-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d576-102">SYNOPSIS</span></span>
<span data-ttu-id="5d576-103">Резервное копирование службы управления API.</span><span class="sxs-lookup"><span data-stu-id="5d576-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="5d576-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d576-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d576-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d576-105">DESCRIPTION</span></span>
<span data-ttu-id="5d576-106">Командлет **BACKUP-AzApiManagement** является резервным копированием экземпляра службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="5d576-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="5d576-107">Этот командлет хранит резервную копию как BLOB-объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5d576-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="5d576-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d576-108">EXAMPLES</span></span>

### <span data-ttu-id="5d576-109">Пример 1: создание резервной копии службы управления API</span><span class="sxs-lookup"><span data-stu-id="5d576-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="5d576-110">Эта команда позволяет выполнить резервное копирование службы управления API в большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d576-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="5d576-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d576-111">PARAMETERS</span></span>

### <span data-ttu-id="5d576-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d576-112">-DefaultProfile</span></span>
<span data-ttu-id="5d576-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d576-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d576-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d576-114">-Name</span></span>
<span data-ttu-id="5d576-115">Указывает имя развертывания управления API, которое этот командлет зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="5d576-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="5d576-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d576-116">-PassThru</span></span>
<span data-ttu-id="5d576-117">Указывает на то, что этот командлет возвращает резервный объект **PsApiManagement** , если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5d576-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="5d576-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d576-118">-ResourceGroupName</span></span>
<span data-ttu-id="5d576-119">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="5d576-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="5d576-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="5d576-120">-StorageContext</span></span>
<span data-ttu-id="5d576-121">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="5d576-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="5d576-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="5d576-122">-TargetBlobName</span></span>
<span data-ttu-id="5d576-123">Указывает имя большого двоичного объекта для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="5d576-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="5d576-124">Если большой двоичный объект не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="5d576-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="5d576-125">Этот командлет создает значение по умолчанию на основе следующего шаблона: {Name}-{гггг-мм-дд-чч-мм}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="5d576-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="5d576-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="5d576-126">-TargetContainerName</span></span>
<span data-ttu-id="5d576-127">Указывает имя контейнера большого двоичного объекта для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="5d576-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="5d576-128">Если контейнер не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="5d576-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="5d576-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d576-129">CommonParameters</span></span>
<span data-ttu-id="5d576-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d576-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d576-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d576-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d576-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d576-132">INPUTS</span></span>

### <span data-ttu-id="5d576-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5d576-133">System.String</span></span>

### <span data-ttu-id="5d576-134">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5d576-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5d576-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d576-135">OUTPUTS</span></span>

### <span data-ttu-id="5d576-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d576-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="5d576-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d576-137">NOTES</span></span>

## <span data-ttu-id="5d576-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d576-138">RELATED LINKS</span></span>

[<span data-ttu-id="5d576-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d576-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="5d576-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d576-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="5d576-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d576-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="5d576-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5d576-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

