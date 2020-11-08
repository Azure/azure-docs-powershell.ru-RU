---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066432"
---
# <span data-ttu-id="9458f-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9458f-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="9458f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9458f-102">SYNOPSIS</span></span>
<span data-ttu-id="9458f-103">Резервное копирование службы управления API.</span><span class="sxs-lookup"><span data-stu-id="9458f-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="9458f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9458f-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9458f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9458f-105">DESCRIPTION</span></span>
<span data-ttu-id="9458f-106">Командлет **BACKUP-AzApiManagement** является резервным копированием экземпляра службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="9458f-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="9458f-107">Этот командлет хранит резервную копию как BLOB-объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="9458f-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="9458f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9458f-108">EXAMPLES</span></span>

### <span data-ttu-id="9458f-109">Пример 1: создание резервной копии службы управления API</span><span class="sxs-lookup"><span data-stu-id="9458f-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="9458f-110">Эта команда позволяет выполнить резервное копирование службы управления API в большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="9458f-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="9458f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9458f-111">PARAMETERS</span></span>

### <span data-ttu-id="9458f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9458f-112">-DefaultProfile</span></span>
<span data-ttu-id="9458f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9458f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9458f-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9458f-114">-Name</span></span>
<span data-ttu-id="9458f-115">Указывает имя развертывания управления API, которое этот командлет зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="9458f-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="9458f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9458f-116">-PassThru</span></span>
<span data-ttu-id="9458f-117">Указывает на то, что этот командлет возвращает резервный объект **PsApiManagement** , если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9458f-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="9458f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9458f-118">-ResourceGroupName</span></span>
<span data-ttu-id="9458f-119">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="9458f-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="9458f-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="9458f-120">-StorageContext</span></span>
<span data-ttu-id="9458f-121">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="9458f-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="9458f-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="9458f-122">-TargetBlobName</span></span>
<span data-ttu-id="9458f-123">Указывает имя большого двоичного объекта для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="9458f-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="9458f-124">Если большой двоичный объект не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="9458f-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="9458f-125">Этот командлет создает значение по умолчанию на основе следующего шаблона: {Name}-{гггг-мм-дд-чч-мм}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="9458f-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="9458f-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="9458f-126">-TargetContainerName</span></span>
<span data-ttu-id="9458f-127">Указывает имя контейнера большого двоичного объекта для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9458f-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="9458f-128">Если контейнер не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="9458f-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="9458f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9458f-129">CommonParameters</span></span>
<span data-ttu-id="9458f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9458f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9458f-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9458f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9458f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9458f-132">INPUTS</span></span>

### <span data-ttu-id="9458f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9458f-133">System.String</span></span>

### <span data-ttu-id="9458f-134">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9458f-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9458f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9458f-135">OUTPUTS</span></span>

### <span data-ttu-id="9458f-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9458f-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9458f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9458f-137">NOTES</span></span>

## <span data-ttu-id="9458f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9458f-138">RELATED LINKS</span></span>

[<span data-ttu-id="9458f-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9458f-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="9458f-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9458f-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="9458f-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9458f-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="9458f-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9458f-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


