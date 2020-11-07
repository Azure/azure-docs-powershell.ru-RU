---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913105"
---
# <span data-ttu-id="ac87c-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="ac87c-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="ac87c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac87c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac87c-103">Изменяет версию операционной системы для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="ac87c-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="ac87c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac87c-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac87c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac87c-105">DESCRIPTION</span></span>
<span data-ttu-id="ac87c-106">Командлет **Set-AzBatchPoolOSVersion** изменяет версию операционной системы для указанного пула.</span><span class="sxs-lookup"><span data-stu-id="ac87c-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="ac87c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac87c-107">EXAMPLES</span></span>

### <span data-ttu-id="ac87c-108">Пример 1: Установка целевой версии операционной системы для пула</span><span class="sxs-lookup"><span data-stu-id="ac87c-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="ac87c-109">Эта команда задает целевую версию операционной системы для пула MyPool на WA-GUEST-OS-4.20 _201505-01.</span><span class="sxs-lookup"><span data-stu-id="ac87c-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="ac87c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac87c-110">PARAMETERS</span></span>

### <span data-ttu-id="ac87c-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ac87c-111">-BatchContext</span></span>
<span data-ttu-id="ac87c-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ac87c-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ac87c-113">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="ac87c-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ac87c-114">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ac87c-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ac87c-115">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="ac87c-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ac87c-116">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ac87c-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ac87c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac87c-117">-DefaultProfile</span></span>
<span data-ttu-id="ac87c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac87c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac87c-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ac87c-119">-Id</span></span>
<span data-ttu-id="ac87c-120">Указывает идентификатор пула.</span><span class="sxs-lookup"><span data-stu-id="ac87c-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="ac87c-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="ac87c-121">-TargetOSVersion</span></span>
<span data-ttu-id="ac87c-122">Указывает версию гостевой операционной системы Azure для установки на виртуальных машинах в пуле.</span><span class="sxs-lookup"><span data-stu-id="ac87c-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="ac87c-123">Дополнительные сведения о версиях гостевой операционной системы Azure можно найти в выпусках Azure Guest OS и в матрице совместимости SDK https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="ac87c-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="ac87c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac87c-124">CommonParameters</span></span>
<span data-ttu-id="ac87c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac87c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac87c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac87c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac87c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac87c-127">INPUTS</span></span>

### <span data-ttu-id="ac87c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ac87c-128">System.String</span></span>

### <span data-ttu-id="ac87c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ac87c-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ac87c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac87c-130">OUTPUTS</span></span>

### <span data-ttu-id="ac87c-131">System. void</span><span class="sxs-lookup"><span data-stu-id="ac87c-131">System.Void</span></span>

## <span data-ttu-id="ac87c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac87c-132">NOTES</span></span>

## <span data-ttu-id="ac87c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac87c-133">RELATED LINKS</span></span>

[<span data-ttu-id="ac87c-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ac87c-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


