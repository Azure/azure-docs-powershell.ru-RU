---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568239"
---
# <span data-ttu-id="05654-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="05654-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="05654-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05654-102">SYNOPSIS</span></span>
<span data-ttu-id="05654-103">Изменяет версию операционной системы для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="05654-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05654-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05654-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05654-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05654-105">DESCRIPTION</span></span>
<span data-ttu-id="05654-106">Командлет **Set-AzureBatchPoolOSVersion** изменяет версию операционной системы для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="05654-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="05654-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05654-107">EXAMPLES</span></span>

### <span data-ttu-id="05654-108">Пример 1: Установка целевой версии операционной системы для пула</span><span class="sxs-lookup"><span data-stu-id="05654-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="05654-109">Эта команда задает целевую версию операционной системы для пула MyPool на WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="05654-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="05654-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05654-110">PARAMETERS</span></span>

### <span data-ttu-id="05654-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="05654-111">-BatchContext</span></span>
<span data-ttu-id="05654-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="05654-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="05654-113">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="05654-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="05654-114">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="05654-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="05654-115">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="05654-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="05654-116">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="05654-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05654-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05654-117">-DefaultProfile</span></span>
<span data-ttu-id="05654-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05654-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05654-119">-ID</span><span class="sxs-lookup"><span data-stu-id="05654-119">-Id</span></span>
<span data-ttu-id="05654-120">Указывает идентификатор пула.</span><span class="sxs-lookup"><span data-stu-id="05654-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05654-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="05654-121">-TargetOSVersion</span></span>
<span data-ttu-id="05654-122">Указывает версию гостевой операционной системы Azure для установки на виртуальных машинах в пуле.</span><span class="sxs-lookup"><span data-stu-id="05654-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="05654-123">Дополнительные сведения о версиях гостевой операционной системы Azure можно найти в выпусках Azure Guest OS и в матрице совместимости SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="05654-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05654-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05654-124">CommonParameters</span></span>
<span data-ttu-id="05654-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05654-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05654-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05654-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05654-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05654-127">INPUTS</span></span>

### <span data-ttu-id="05654-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="05654-128">BatchAccountContext</span></span>
<span data-ttu-id="05654-129">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="05654-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="05654-130">Подстрок</span><span class="sxs-lookup"><span data-stu-id="05654-130">String</span></span>
<span data-ttu-id="05654-131">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="05654-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="05654-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05654-132">OUTPUTS</span></span>

## <span data-ttu-id="05654-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="05654-133">NOTES</span></span>

## <span data-ttu-id="05654-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05654-134">RELATED LINKS</span></span>

[<span data-ttu-id="05654-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="05654-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


