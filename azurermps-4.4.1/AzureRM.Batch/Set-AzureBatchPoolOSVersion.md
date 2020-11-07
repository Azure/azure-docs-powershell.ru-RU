---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733406"
---
# <span data-ttu-id="dfbdc-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="dfbdc-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="dfbdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbdc-103">Изменяет версию операционной системы для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfbdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfbdc-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfbdc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="dfbdc-106">Командлет **Set-AzureBatchPoolOSVersion** изменяет версию операционной системы для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="dfbdc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="dfbdc-108">Пример 1: Установка целевой версии операционной системы для пула</span><span class="sxs-lookup"><span data-stu-id="dfbdc-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="dfbdc-109">Эта команда задает целевую версию операционной системы для пула MyPool на WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="dfbdc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfbdc-110">PARAMETERS</span></span>

### <span data-ttu-id="dfbdc-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dfbdc-111">-BatchContext</span></span>
<span data-ttu-id="dfbdc-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dfbdc-113">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbdc-114">-ID</span><span class="sxs-lookup"><span data-stu-id="dfbdc-114">-Id</span></span>
<span data-ttu-id="dfbdc-115">Указывает идентификатор пула.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-115">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbdc-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="dfbdc-116">-TargetOSVersion</span></span>
<span data-ttu-id="dfbdc-117">Указывает версию гостевой операционной системы Azure для установки на виртуальных машинах в пуле.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="dfbdc-118">Дополнительные сведения о версиях гостевой операционной системы Azure можно найти в выпусках Azure Guest OS и в матрице совместимости SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="dfbdc-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbdc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbdc-119">-DefaultProfile</span></span>
<span data-ttu-id="dfbdc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfbdc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbdc-121">CommonParameters</span></span>
<span data-ttu-id="dfbdc-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbdc-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbdc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbdc-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfbdc-124">INPUTS</span></span>

### <span data-ttu-id="dfbdc-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dfbdc-125">BatchAccountContext</span></span>
<span data-ttu-id="dfbdc-126">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="dfbdc-127">Подстрок</span><span class="sxs-lookup"><span data-stu-id="dfbdc-127">String</span></span>
<span data-ttu-id="dfbdc-128">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dfbdc-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dfbdc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfbdc-129">OUTPUTS</span></span>

## <span data-ttu-id="dfbdc-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfbdc-130">NOTES</span></span>

## <span data-ttu-id="dfbdc-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfbdc-131">RELATED LINKS</span></span>

[<span data-ttu-id="dfbdc-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dfbdc-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


