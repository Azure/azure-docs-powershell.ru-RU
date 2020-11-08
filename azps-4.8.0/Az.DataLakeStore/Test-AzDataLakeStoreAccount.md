---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236771"
---
# <span data-ttu-id="01a5a-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="01a5a-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="01a5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="01a5a-103">Проверка наличия учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="01a5a-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="01a5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01a5a-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01a5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="01a5a-106">Командлет **Test-AzDataLakeStoreAccount** проверяет наличие учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="01a5a-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="01a5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01a5a-107">EXAMPLES</span></span>

### <span data-ttu-id="01a5a-108">Пример 1: Проверка учетной записи</span><span class="sxs-lookup"><span data-stu-id="01a5a-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="01a5a-109">Эта команда проверяет, существует ли учетная запись с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="01a5a-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="01a5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01a5a-110">PARAMETERS</span></span>

### <span data-ttu-id="01a5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a5a-111">-DefaultProfile</span></span>
<span data-ttu-id="01a5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01a5a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01a5a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01a5a-113">-Name</span></span>
<span data-ttu-id="01a5a-114">Указывает имя учетной записи Data Lake Store для проверки.</span><span class="sxs-lookup"><span data-stu-id="01a5a-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a5a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a5a-115">-ResourceGroupName</span></span>
<span data-ttu-id="01a5a-116">Указывает имя группы ресурсов, которая содержит учетную запись для проверки.</span><span class="sxs-lookup"><span data-stu-id="01a5a-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a5a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a5a-117">CommonParameters</span></span>
<span data-ttu-id="01a5a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01a5a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a5a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a5a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a5a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01a5a-120">INPUTS</span></span>

### <span data-ttu-id="01a5a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="01a5a-121">System.String</span></span>

## <span data-ttu-id="01a5a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01a5a-122">OUTPUTS</span></span>

### <span data-ttu-id="01a5a-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01a5a-123">System.Boolean</span></span>

## <span data-ttu-id="01a5a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="01a5a-124">NOTES</span></span>

## <span data-ttu-id="01a5a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01a5a-125">RELATED LINKS</span></span>

[<span data-ttu-id="01a5a-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="01a5a-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="01a5a-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="01a5a-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="01a5a-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="01a5a-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="01a5a-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="01a5a-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


