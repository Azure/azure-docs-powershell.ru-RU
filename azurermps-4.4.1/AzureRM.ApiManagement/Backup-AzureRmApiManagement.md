---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d036b31f521736420b91b04b4f6f5513f3dbc50d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567195"
---
# <span data-ttu-id="8c25f-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c25f-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="8c25f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c25f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c25f-103">Резервное копирование службы управления API.</span><span class="sxs-lookup"><span data-stu-id="8c25f-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c25f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c25f-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c25f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c25f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c25f-106">Командлет **BACKUP-AzureRmApiManagement** является резервным копированием экземпляра службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="8c25f-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="8c25f-107">Этот командлет хранит резервную копию как BLOB-объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8c25f-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="8c25f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c25f-108">EXAMPLES</span></span>

### <span data-ttu-id="8c25f-109">Пример 1: создание резервной копии службы управления API</span><span class="sxs-lookup"><span data-stu-id="8c25f-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="8c25f-110">Эта команда позволяет выполнить резервное копирование службы управления API в большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="8c25f-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="8c25f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c25f-111">PARAMETERS</span></span>

### <span data-ttu-id="8c25f-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c25f-112">-Name</span></span>
<span data-ttu-id="8c25f-113">Указывает имя развертывания управления API, которое этот командлет зарезервировать.</span><span class="sxs-lookup"><span data-stu-id="8c25f-113">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="8c25f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c25f-114">-PassThru</span></span>
<span data-ttu-id="8c25f-115">Указывает на то, что этот командлет возвращает резервный объект **PsApiManagement** , если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8c25f-115">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="8c25f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c25f-116">-ResourceGroupName</span></span>
<span data-ttu-id="8c25f-117">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="8c25f-117">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="8c25f-118">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="8c25f-118">-StorageContext</span></span>
<span data-ttu-id="8c25f-119">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="8c25f-119">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="8c25f-120">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="8c25f-120">-TargetBlobName</span></span>
<span data-ttu-id="8c25f-121">Указывает имя большого двоичного объекта для резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8c25f-121">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="8c25f-122">Если большой двоичный объект не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="8c25f-122">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="8c25f-123">Этот командлет создает значение по умолчанию на основе следующего шаблона:</span><span class="sxs-lookup"><span data-stu-id="8c25f-123">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="8c25f-124">{Name}-{гггг-мм-дд-чч-мм}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="8c25f-124">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="8c25f-125">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="8c25f-125">-TargetContainerName</span></span>
<span data-ttu-id="8c25f-126">Указывает имя контейнера большого двоичного объекта для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8c25f-126">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="8c25f-127">Если контейнер не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="8c25f-127">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="8c25f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c25f-128">-DefaultProfile</span></span>
<span data-ttu-id="8c25f-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c25f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c25f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c25f-130">CommonParameters</span></span>
<span data-ttu-id="8c25f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c25f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c25f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c25f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c25f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c25f-133">INPUTS</span></span>

## <span data-ttu-id="8c25f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c25f-134">OUTPUTS</span></span>

### <span data-ttu-id="8c25f-135">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c25f-135">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8c25f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c25f-136">NOTES</span></span>

## <span data-ttu-id="8c25f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c25f-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c25f-138">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c25f-138">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="8c25f-139">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c25f-139">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="8c25f-140">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c25f-140">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="8c25f-141">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8c25f-141">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


