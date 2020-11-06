---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568012"
---
# <span data-ttu-id="992f1-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="992f1-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="992f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="992f1-102">SYNOPSIS</span></span>
<span data-ttu-id="992f1-103">Проверка наличия учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="992f1-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="992f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="992f1-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="992f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="992f1-105">DESCRIPTION</span></span>
<span data-ttu-id="992f1-106">Командлет **Test-AzureRmDataLakeStoreAccount** проверяет наличие учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="992f1-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="992f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="992f1-107">EXAMPLES</span></span>

### <span data-ttu-id="992f1-108">Пример 1: Проверка учетной записи</span><span class="sxs-lookup"><span data-stu-id="992f1-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="992f1-109">Эта команда проверяет, существует ли учетная запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="992f1-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="992f1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="992f1-110">PARAMETERS</span></span>

### <span data-ttu-id="992f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992f1-111">-DefaultProfile</span></span>
<span data-ttu-id="992f1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="992f1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="992f1-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="992f1-113">-Name</span></span>
<span data-ttu-id="992f1-114">Указывает имя учетной записи Data Lake Store для проверки.</span><span class="sxs-lookup"><span data-stu-id="992f1-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992f1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992f1-115">-ResourceGroupName</span></span>
<span data-ttu-id="992f1-116">Указывает имя группы ресурсов, которая содержит учетную запись для проверки.</span><span class="sxs-lookup"><span data-stu-id="992f1-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="992f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992f1-117">CommonParameters</span></span>
<span data-ttu-id="992f1-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="992f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992f1-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992f1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992f1-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="992f1-120">INPUTS</span></span>

### <span data-ttu-id="992f1-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="992f1-121">None</span></span>
<span data-ttu-id="992f1-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="992f1-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="992f1-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="992f1-123">OUTPUTS</span></span>

### <span data-ttu-id="992f1-124">логических</span><span class="sxs-lookup"><span data-stu-id="992f1-124">bool</span></span>
<span data-ttu-id="992f1-125">Значение true или false, указывающее на существование указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="992f1-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="992f1-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="992f1-126">NOTES</span></span>

## <span data-ttu-id="992f1-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="992f1-127">RELATED LINKS</span></span>

[<span data-ttu-id="992f1-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="992f1-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="992f1-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="992f1-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="992f1-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="992f1-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="992f1-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="992f1-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


