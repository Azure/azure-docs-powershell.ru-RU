---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732076"
---
# <span data-ttu-id="2e4c9-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e4c9-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="2e4c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e4c9-103">Восстанавливает службу управления API из указанного блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e4c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e4c9-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e4c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="2e4c9-106">Командлет **RESTORE-AzureRmApiManagement** восстанавливает службу управления API из указанного резервного копирования, расположенного в большом двоичном объекте Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="2e4c9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e4c9-107">EXAMPLES</span></span>

### <span data-ttu-id="2e4c9-108">Пример 1: восстановление службы управления API</span><span class="sxs-lookup"><span data-stu-id="2e4c9-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="2e4c9-109">Эта команда восстанавливает службу управления API из большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="2e4c9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e4c9-110">PARAMETERS</span></span>

### <span data-ttu-id="2e4c9-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e4c9-111">-Name</span></span>
<span data-ttu-id="2e4c9-112">Указывает имя экземпляра управления API, который будет восстановлен вместе с резервной копией.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="2e4c9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e4c9-113">-PassThru</span></span>
<span data-ttu-id="2e4c9-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e4c9-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e4c9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e4c9-116">-ResourceGroupName</span></span>
<span data-ttu-id="2e4c9-117">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="2e4c9-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="2e4c9-118">-SourceBlobName</span></span>
<span data-ttu-id="2e4c9-119">Указывает имя блоба источника резервного копирования хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="2e4c9-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="2e4c9-120">-SourceContainerName</span></span>
<span data-ttu-id="2e4c9-121">Указывает имя контейнера источника резервной копии хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="2e4c9-122">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="2e4c9-122">-StorageContext</span></span>
<span data-ttu-id="2e4c9-123">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-123">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e4c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e4c9-124">-DefaultProfile</span></span>
<span data-ttu-id="2e4c9-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e4c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e4c9-126">CommonParameters</span></span>
<span data-ttu-id="2e4c9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e4c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e4c9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e4c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e4c9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e4c9-129">INPUTS</span></span>

## <span data-ttu-id="2e4c9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e4c9-130">OUTPUTS</span></span>

### <span data-ttu-id="2e4c9-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e4c9-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2e4c9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e4c9-132">NOTES</span></span>

## <span data-ttu-id="2e4c9-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e4c9-133">RELATED LINKS</span></span>

[<span data-ttu-id="2e4c9-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e4c9-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="2e4c9-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e4c9-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="2e4c9-136">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e4c9-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="2e4c9-137">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2e4c9-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


